//Задайте произвольный массив. Выведете его элементы, начиная 
//с конца. Использовать рекурсию, не использовать циклы

int[] number = { 2, 2, 6, 7, 8, 8, 1, 2, 3, 9 };
int count = 0;

void PrintEnd(int[] array, int i)
{
    if (i == array.Length)
    {
        return;
    }
    PrintEnd(array, i + 1);
    Console.WriteLine(array[i]);
}

PrintEnd(number, count);

//Напишите программу вычисления функции Аккермана с помощью
 //рекурсии. Даны два неотрицательных числа m и n.

Console.WriteLine("Введите целое неотрицательное число n: ");
int n = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Введите целое неотрицательное число m: ");
int m = Convert.ToInt32(Console.ReadLine());

int ack(int n, int m)
{
    if (n == 0)
    {
        return m + 1;  
    }
    else if (m == 0)
    {
        return ack(n - 1, 1);
    }
    else 
    {
        return ack(n - 1, ack(n, m - 1));
    }
}
Console.WriteLine($"Результат выполнения функции Аккермана: {ack(n,m)}");
