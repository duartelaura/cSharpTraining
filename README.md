# cSharpTraining


----------------------------------------------------------------------------------------------------------------


CALCULAR IMC

using System;

namespace EXERCICIO01
{
    internal class Program
    {
        static void Main(string[] args)
        {
            double peso, altura, imc;

            Console.WriteLine("Digite o seu peso em quilos: ");
            peso = double.Parse(Console.ReadLine());

            Console.WriteLine("Digite a sua altura em metros: ");
            altura = double.Parse(Console.ReadLine());

            imc = peso / (altura * altura);

            if (imc <= 18.5)
            {
                Console.WriteLine($"Seu IMC é {imc:F2} - abaixo do peso");
            }
            else if (imc < 24.9)
            {
                Console.WriteLine($"Seu IMC é {imc:F2} - peso normal");
            }
            else if (imc < 29.9)
            {
                Console.WriteLine($"Seu IMC é {imc:F2} - sobrepeso");
            }
            else if (imc < 34.9)
            {
                Console.WriteLine($"Seu IMC é {imc:F2} - obesidade 1");
            }
            else if (imc < 39.9)
            {
                Console.WriteLine($"Seu IMC é {imc:F2} - obesidade 2 (severa)");
            }
            else if (imc >= 40)
            {
                Console.WriteLine($"Seu IMC é {imc:F2} - obesidade 3 (mórbida)");
            }

            Console.WriteLine("Pressione qualquer tecla para sair.");

            Console.ReadKey();
        }


----------------------------------------------------------------------------------------------------------------


LISTA 01 ATP



/**
* PUC Minas, Campus Barreiro
* ATP - Aula Prática
* Data: 20/08/2025 (quarta-feira)
* @author Laura Duarte Resende
* Objetivo: praticar a criação de variáveis e tipos no C#.
* Data e descrição da última manutenção: 21/08/2025 - Início da lista.
*/

using System;

namespace LISTA01_ATP
{
    internal class Exercicio01
    {
        static void Main(string[] args)
        {

            /*  1.  Faça um programa que receba duas notas, calcule e mostre a média ponderada dessas notas,
                    considerando peso 2 para a primeira nota e peso 3 para a segunda nota.
                    Média = (Nota1 × Peso1 + Nota2 × Peso2) ÷ (Peso1 + Peso2) */

            double nota1, nota2, media;

            Console.WriteLine("Digite a primeira nota: ");
            nota1 = double.Parse(Console.ReadLine());

            Console.WriteLine("Digite a segunda nota: ");
            nota2 = double.Parse(Console.ReadLine());

            media = ((nota1 * 2) + (nota2 * 3)) / (2 + 3);
            Console.WriteLine($"A média ponderada é: {media:F1} \nPressione qualquer tecla para sair");
            Console.ReadKey();

        }

        static void Exercicio02()
        {
            /*  2.  Faça um programa que receba o preço de um produto, calcule e mostre o novo preço, sabendo-se
                    que este sofreu um desconto de 10%.*/

            double precoProduto, novoPreco;

            Console.WriteLine("Digite o preço do produto: ");
            precoProduto = double.Parse(Console.ReadLine());

            novoPreco = precoProduto - ((precoProduto / 100) * 10);
            Console.WriteLine($"O novo preço é: {novoPreco:F2} \nPressione qualquer tecla para sair");
            Console.ReadKey();
        }

        static void Exercicio03()
        {
            /*  03. Faça um programa que calcule e mostre a área de um trapézio. Sabe-se que:
                    𝐴𝑟𝑒𝑎 = (𝑏𝑎𝑠𝑒 𝑚𝑎𝑖𝑜𝑟 + 𝑏𝑎𝑠𝑒 𝑚𝑒𝑛𝑜𝑟). 𝑎𝑙𝑡𝑢𝑟𝑎 2*/

            double baseMaior, baseMenor, altura, area;
            Console.WriteLine("Digite o valor da base maior: ");
            baseMaior = double.Parse(Console.ReadLine());

            Console.WriteLine("Digite o valor da base menor: ");
            baseMenor = double.Parse(Console.ReadLine());

            Console.WriteLine("Digite o valor da altura: ");
            altura = double.Parse(Console.ReadLine());

            area = ((baseMaior + baseMenor) * altura) / 2;

            Console.WriteLine($"A área do trapézio é: {area:F2} \nPressione qualquer tecla para sair");
            Console.ReadKey();

        }

        static void Exercicio04()
        {
            /*  4. Faça um programa que receba o valor do salário mínimo atual e o valor do salário de um
                funcionário, calcule e mostre a quantidade de salários mínimos que ganha esse funcionário.*/

            double salarioMinimo, salarioFuncionario, qtdSalarios;

            Console.WriteLine("Digite o valor do salário mínimo: ");
            salarioMinimo = double.Parse(Console.ReadLine());

            Console.WriteLine("Digite o valor do salário do funcionário: ");
            salarioFuncionario = double.Parse(Console.ReadLine());

            qtdSalarios = salarioFuncionario / salarioMinimo;

            Console.WriteLine($"O funcionário recebe {qtdSalarios:F2} salário(s) mínimos \nPressione qualquer tecla para sair");
            Console.ReadKey();

        }

        static void Exercicio05()
        {
            /*  5. Faça um programa que receba o raio, calcule e mostre:
                a) o comprimento de uma esfera, sabe-se que C = 2πR;
                b) a área de uma esfera, sabe-se que A = πR2;
                c) o volume de uma esfera, sabe-se que V = 4/3πR3.
                Obs: Para calcular o raio ao quadrado ou ao cubo você pode usar a função Pow() como
                abaixo:
                Z = Math.Pow(x, y) // calcula a potência: XY e coloca o resultado na variável Z.*/

            double raio, comprimento, area, volume;

            Console.WriteLine("Digite o raio: ");
            raio = double.Parse(Console.ReadLine());

            comprimento = (2 * Math.PI) * raio;

            area = Math.PI * Math.Pow(raio, 2);

            volume = (4.0 / 3.0) * Math.PI * Math.Pow(raio, 3);

            Console.WriteLine($"Comprimento: {comprimento:F2} \nÁrea: {area:F2} \nVolume:{volume:F2} \nPressione qualquer tecla para sair");
            Console.ReadKey();

        }

        static void Exercicio06()
        {
            /*  6. Faça um programa que receba a medida de dois ângulos de um triângulo, calcule e mostre a
                medida do terceiro ângulo. Sabe-se que a soma dos ângulos de um triângulo é 180.*/

            double angulo1, angulo2, angulo3;

            Console.WriteLine("Digite o primeiro ângulo: ");
            angulo1 = double.Parse(Console.ReadLine());

            Console.WriteLine("Digite o segundo ângulo: ");
            angulo2 = double.Parse(Console.ReadLine());

            angulo3 = 180 - (angulo1 + angulo2);

            Console.WriteLine($"O terceiro ângulo é: {angulo3:F1} \nPressione qualquer tecla para sair");
            Console.ReadKey();

        }

        static void Exercicio07()
        {
            /*  7. Fazer um programa que receba os três coeficientes de uma equação do segundo grau e calcule
                as suas raízes. Suponha que só serão informadas equações com raízes reais.*/

            double c1, c2, c3, r1, r2 , r3;

            Console.WriteLine("Digite o primeiro coeficiente: ");
            c1 = double.Parse(Console.ReadLine());

            Console.WriteLine("Digite o segundo coeficiente: ");
            c2 = double.Parse(Console.ReadLine());

            Console.WriteLine("Digite o terceiro coeficiente: ");
            c3 = double.Parse(Console.ReadLine());

            r1 = Math.Sqrt(c1);

            r2 = Math.Sqrt(c2);

            r3 = Math.Sqrt(c3);

            Console.WriteLine($"\nA raíz do primeiro coeficiente é: {r1:F0}\n" +
                $"A raíz do segundo coeficiente é: {r2:F0}\n" +
                $"A raíz do terceiro coeficiente é: {r3:F0}\n \nPressione qualquer tecla para sair");
            Console.ReadKey();

        }
    }
}

    }
}


