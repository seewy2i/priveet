using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

class Program
{
    static void Main()
    {
        // Создаем список строк
        List<string> strings = new List<string> { "Привет", "мир", "это", "C#", "привет", "мир", "это", "C#" };

        // Создаем словарь для хранения частоты каждого слова
        Dictionary<string, int> wordFrequency = new Dictionary<string, int>();

        // Проходим по каждому слову в списке
        foreach (string word in strings)
        {
            // Если слово уже есть в словаре, увеличиваем его частоту на 1
            if (wordFrequency.ContainsKey(word))
            {
                wordFrequency[word]++;
            }
            // Если слово еще не в словаре, добавляем его с частотой 1
            else
            {
                wordFrequency.Add(word, 1);
            }
        }

        // Выводим слова и их частоту
        foreach (KeyValuePair<string, int> pair in wordFrequency)
        {
            Console.WriteLine($"{pair.Key} - {pair.Value}");
        }

        Console.ReadKey();
    }
}

