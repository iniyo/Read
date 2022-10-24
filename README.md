- 👋 Hi, I’m @iniyo
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...


2022.09.08 C# 수업 예제
using System;
//class IdentifierApp {
//    public static void Main() {
//        int MyVar = 1, myvar = 2;
//        int @int = 10, 변수 = 20;
//        Console.WriteLine("MyVar = " + MyVar + ", myvar = " + myvar);
//        Console.WriteLine("@int = " + @int + ", 변수 = " + 변수);
//    }
//}

/*예제 3-20*/
//class SimpleIOApp {
//    public static void Main() {
//        int i; char c;
//        Console.Write("Enter a digit and a character = ");
//        i = Console.Read() - 48; // ‘0’ = 48 (문자 코드 값 )
//        c = (char)Console.Read(); // (char) : casting 연산자 : casting은 dummy
//        Console.Write("i = " + i);
//        Console.WriteLine(", c = " + c);
//    }
//}

/*예제 3-21*/
//class ReadLineApp {
//    public static void Main() {
//        int time, hour, minute, second;
//        Console.WriteLine("***Enter an integral time: ");
//        time = int.Parse(Console.ReadLine());
//        hour = time / 10000;
//        minute = time / 100 % 100;
//        second = time % 100;
//        Console.WriteLine("***Time is " + hour + ":" + minute + ":" + second);
//    }
//}

/*예제 3-22*/
class ReadIntegerApp {
    static int ReadInt() {
        char ch;
        int n = 0;
        while (!char.IsDigit(ch = (char)Console.Read())) ;
        do {
            n = n * 10 + (ch - '0');
            ch = (char)Console.Read();
        } while (char.IsDigit(ch)); // 숫자가 아닌 글자 입력 시 벗어남
        return n;
    }
    public static void Main() {
        Console.Write("*** input data : ");
        Console.WriteLine("*** read data : " + ReadInt() + " " + ReadInt());
    }
}

/* 표준입출력 3장 예제 (책x)*/
namespace standard_output_2 {
    class Program {
        static void Main(string[] args) {
            double a = 3;
            double b = 4;
            Console.WriteLine("Pythagorean Theory of {0} and {1}:", a, b);
            Console.WriteLine("Geometric ={0,12:F3}", Math.Sqrt(a * a + b * b));
            Console.WriteLine("Geometric ={0:F3}", Math.Sqrt(a * a + b * b));
            double k = 3.4567;
            Console.WriteLine("Percent Value = {0, 10:P3}", k);
            Console.WriteLine("Percent Value = {0:P3}", k);
            int value = 34561234;
            Console.WriteLine("decimal Value = {0, -15:D}", value
            Console.WriteLine("decimal Value = {0:D10}", value);
        }
    }
}

/*예제 3-23*/
//class FormattedOutputApp {
//    public static void Main() {
//        Console.WriteLine("1) {0,-5},{1,5},{2,5}", 1.2, 1.2, 123.45);
//        double d = Math.PI;
//        Console.WriteLine("2) {0}", d);
//        Console.WriteLine("3) {0:C}", d);
//        Console.WriteLine("4) {0:E}", d);
//        Console.WriteLine("5) {0:F}", d);
//        Console.WriteLine("6) {0:G}", d);
//        Console.WriteLine("7) {0:P}", d);
//        Console.WriteLine("8) {0:R}", d);
//        Console.WriteLine("9) {0:X}", 255);
//    }
//}

/*예제 2-2*/
class IntegerConstantApp {
    public static void Main() {
        int i = 255, h = 0Xff; //16진수 표기
        long l = 0XffL; // long형
        Console.WriteLine("i = {0}, h = {1}", i, h);
        if (h == l) Console.WriteLine("Yes");
        else Console.WriteLine("No");
    }
}

/*예제 2-3*/
class RealConstantApp {
    public static void Main() {
        float f1 = 1.414F, f2 = 0.1414e01f;
        double d = 0.1414E1;
        Console.WriteLine("f1 = " + f1 + ", f2 = " + f2 + ", d = " + d);
        if (f1 == f2) Console.WriteLine("Yes");
        else Console.WriteLine("No");
    }
}
