<!DOCTYPE html>
<html>
<head>
    <title>Операции над матрицами в C</title>
</head>
<body>
    <h1>Операции над матрицами в C</h1>

    <h2>Описание проекта</h2>
    <p>Этот проект представляет собой реализацию операций над матрицами с использованием языка программирования C. В рамках проекта реализованы различные операции, такие как создание, удаление, сравнение, сложение, вычитание, умножение, транспонирование, вычисление миноров, определителей и обратных матриц для матриц разных размеров.</p>

    <h2>Структура матрицы</h2>
    <p>Для представления матриц в проекте используется следующая C-структура:</p>
    <pre>
        <code>
typedef struct matrix_struct {
    double** matrix;
    int rows;
    int columns;
} matrix_t;
        </code>
    </pre>

    <h2>Операции</h2>
    <p>Проект предоставляет следующие операции над матрицами:</p>

    <ol>
        <li><strong>Создание матрицы</strong> (create_matrix):</li>
        <pre>
            <code>
int s21_create_matrix(int rows, int columns, matrix_t *result);
            </code>
        </pre>

        <li><strong>Очистка матрицы</strong> (remove_matrix):</li>
        <pre>
            <code>
void s21_remove_matrix(matrix_t *A);
            </code>
        </pre>

        <li><strong>Сравнение матриц</strong> (eq_matrix):</li>
        <pre>
            <code>
int s21_eq_matrix(matrix_t *A, matrix_t *B);
            </code>
        </pre>

        <li><strong>Сложение матриц</strong> (sum_matrix) и <strong>вычитание матриц</strong> (sub_matrix):</li>
        <pre>
            <code>
int s21_sum_matrix(matrix_t *A, matrix_t *B, matrix_t *result);
int s21_sub_matrix(matrix_t *A, matrix_t *B, matrix_t *result);
            </code>
        </pre>

        <li><strong>Умножение матрицы на число</strong> (mult_number) и <strong>умножение двух матриц</strong> (mult_matrix):</li>
        <pre>
            <code>
int s21_mult_number(matrix_t *A, double number, matrix_t *result);
int s21_mult_matrix(matrix_t *A, matrix_t *B, matrix_t *result);
            </code>
        </pre>

        <li><strong>Транспонирование матрицы</strong> (transpose):</li>
        <pre>
            <code>
int s21_transpose(matrix_t *A, matrix_t *result);
            </code>
        </pre>

        <li><strong>Вычисление миноров матрицы и матрицы алгебраических дополнений</strong> (calc_complements):</li>
        <pre>
            <code>
int s21_calc_complements(matrix_t *A, matrix_t *result);
            </code>
        </pre>

        <li><strong>Вычисление определителя матрицы</strong> (determinant):</li>
        <pre>
            <code>
int s21_determinant(matrix_t *A, double *result);
            </code>
        </pre>

        <li><strong>Вычисление обратной матрицы</strong> (inverse_matrix):</li>
        <pre>
            <code>
int s21_inverse_matrix(matrix_t *A, matrix_t *result);
            </code>
        </pre>
    </ol>

    <h2>Результаты операций</h2>
    <p>Все операции (кроме сравнения матриц) возвращают результирующий код:</p>

    <ul>
        <li><code>0</code> - Операция выполнена успешно</li>
        <li><code>1</code> - Ошибка, некорректная матрица</li>
        <li><code>2</code> - Ошибка вычисления (несовпадающие размеры матриц и другие случаи)</li>
    </ul>

    <h2>Примеры</h2>
    <p>Примеры операций над матрицами и их результаты:</p>
    <pre>
        <code>
matrix_t A, B, C;  // Определение матриц A, B и C

s21_create_matrix(3, 3, &A);  // Создание матрицы A

// Инициализация значений матрицы A

s21_create_matrix(3, 3, &B);  // Создание матрицы B

// Инициализация значений матрицы B

s21_sum_matrix(&A, &B, &C);  // Сложение матриц A и B, результат в матрице C
        </code>
    </pre>

    <h2>Заключение</h2>
    <p>Данный проект позволяет выполнять разнообразные операции над матрицами, включая создание, удаление, сравнение, сложение, вычитание, умножение, транспонирование, вычисление миноров, определителей и обратных матриц. Проект также обеспечивает проверку согласованности размеров матриц и возвращает результирующий код операции для удобства обработки ошибок.</p>
</body>
</html>
