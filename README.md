using System;

namespace text_adventure
{
    class Program
    {
        private static string secChoice;

        static void Main(string[] args)
        {
            gameTitle();
            first();
        }
        public static void gameTitle()
        {
            Console.WriteLine("Welcome to my game");
            Console.WriteLine("Press 'Enter' to begin");
            Console.ReadLine();
            Console.Clear();
            first();
        }

        public static void first()
        {
            string Choice;
            Console.WriteLine("you wake up in a dark cave in a prison");
            Console.WriteLine("What do you do");
            Console.WriteLine("1.try to escape");
            Console.WriteLine("2 cry");
            Console.WriteLine("Pee a little");
            Console.Write("Choice:  ");
            Choice = Console.ReadLine().ToLower();
            Console.Clear();

            switch (Choice)
            {
                case "1":
                case "try to escape":
                case "escape":
                    {
                        Console.WriteLine("you try to escape");
                        Console.WriteLine("the gaurd sees you trying to escape");
                        Console.WriteLine("you have been tased");
                        Console.WriteLine("you faild to escape");
                        Console.WriteLine("press 'ENTER' to continue");
                        Console.ReadLine();
                        gameOver();
                        break;

                    }
                case "2":
                case "cry":
                    {
                        Console.WriteLine("you cry until you fall asleep");
                        Console.WriteLine("the gaurd took you out and let you go and escape");
                        Console.WriteLine("press 'ENTER' to continue");
                        Console.ReadLine();
                        second();
                        break;
                    }
                case "3":
                case "pee":
                    {
                        Console.WriteLine("you peed");
                        Console.WriteLine("you pee smelld bad so bad that you");
                        Console.WriteLine("you vomit youre organs until you died");
                        Console.WriteLine("press 'ENTER' to continue");
                        Console.ReadLine();
                        gameOver();
                        break;
                    }
                default:
                    {
                        Console.WriteLine("i dont understand that command...");
                        Console.WriteLine("PRESS 'ENTER' TO COnTINUE");
                        Console.ReadLine();
                        first();
                        break;
                    }



            }



            public static void second()
            {
                Random rnd = new Random();
                string[] secOptions =

                    { "you have been released, from prison with no surprices.",
                    " you have been released, in the forest." };

                int randomNumber = rnd.Next(0, 2);
                string secText = secOptions[randomNumber];

                string secChoice;
                Console.WriteLine(secText);
                Console.WriteLine("do you try to hide; YES OR NO");
                Console.WriteLine("Choice:  ");
                secChoice = Console.ReadLine().ToLower();
                if (secChoice == "yes" || secChoice == "y")
                {
                    third();
                }
                else if (secChoice == "no" || secChoice == "n")
                {
                    Console.WriteLine("well youre dead now bye");
                    Console.WriteLine("press 'Enter' to continue");
                    Console.ReadLine();
                    gameOver();

                }
                else
                {
                    Console.WriteLine("i dont understand noob");
                    Console.WriteLine("press 'Enter' to continue");
                    Console.ReadLine();
                    second();
                }
            }
            public static void third()
            {
                int age;
                Console.WriteLine("you hide then all youre freinds and family are there");
                Console.WriteLine("they yell surprise and you rememeber its youre birth day");
                Console.WriteLine("how old are you today");
                Console.Write("age:  ");
                int.TryParse(Console.ReadLine(), out age);
                while (age < 100)
                {
                    Console.WriteLine("seriusly? You look older than that!");
                    Console.WriteLine("How old are you really are?");
                    Console.Write("age:  ");
                    int.TryParse(Console.ReadLine(), out age);
                }

                Console.WriteLine("Wow youre old! You must been held back a lot");
                youWin();
            }
            public static void gameOver()
            {


            }
            public static void youWin()
            {


            }
        }
