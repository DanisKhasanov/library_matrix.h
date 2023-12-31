# Операции над матрицами в C  😊

## Описание проекта

Этот проект представляет собой реализацию операций над матрицами с использованием языка программирования C. В рамках проекта реализованы различные операции, такие как создание, удаление, сравнение, сложение, вычитание, умножение, транспонирование, вычисление миноров, определителей и обратных матриц для матриц разных размеров.

## Структура матрицы

Для представления матриц в проекте используется следующая C-структура:

```c
typedef struct matrix_struct {
    double** matrix;
    int rows;
    int columns;
} matrix_t;
```


## Операции

 Создание матрицы (create_matrix):
```c
int s21_create_matrix(int rows, int columns, matrix_t *result);
```
 Очистка матрицы (remove_matrix):
```c
void s21_remove_matrix(matrix_t *A);
```
Сравнение матриц (eq_matrix):
```c
int s21_eq_matrix(matrix_t *A, matrix_t *B);
```
Сложение матриц (sum_matrix) и вычитание матриц (sub_matrix):
```c
int s21_sum_matrix(matrix_t *A, matrix_t *B, matrix_t *result);
int s21_sub_matrix(matrix_t *A, matrix_t *B, matrix_t *result);
```
Умножение матрицы на число (mult_number) и умножение двух матриц (mult_matrix):
```c
int s21_mult_number(matrix_t *A, double number, matrix_t *result);
int s21_mult_matrix(matrix_t *A, matrix_t *B, matrix_t *result);
```
Транспонирование матрицы (transpose):
```c
int s21_transpose(matrix_t *A, matrix_t *result);
```
Вычисление миноров матрицы и матрицы алгебраических дополнений (calc_complements):
```c
int s21_calc_complements(matrix_t *A, matrix_t *result);
```
Вычисление определителя матрицы (determinant):
```c
int s21_determinant(matrix_t *A, double *result);
```
Вычисление обратной матрицы (inverse_matrix):
```c
int s21_inverse_matrix(matrix_t *A, matrix_t *result);
```

## Результаты операций ✅

Все операции (кроме сравнения матриц) возвращают результирующий код:

- 0 - Операция выполнена успешно
- 1 - Ошибка, некорректная матрица
- 2 - Ошибка вычисления (несовпадающие размеры матриц и другие случаи)
