# refactor-special-number

using System;

class Program

{
int kolkko = int.Parse(Console.ReadLine());
int obshto = 0; int takova = 0; bool toe = false;
for (int ch = 1; ch <= kolkko; ch++)
{
    takova = ch;
    while (ch > 0)
    {
        obshto += ch % 10;
        ch = ch / 10;
    }
    toe = (obshto == 5) || (obshto == 7) || (obshto == 11);
    Console.WriteLine($"{takova} -> {toe}");
    obshto = 0;
    ch = takova;
}
}