using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Student
{
    internal class Student
    {
        private string name;
        private int age;
        private double grade;

        //public Student() { }
        public Student(string name, int age, double grade)
        {
            this.name = name;


            set_age(age);


            set_grade(grade);
        }
        public void set_name(string name)
        {
            this.name = name;

        }
        public string get_name()
        {
            return name;
        }
        public void set_age(int age)
        {
            if (age >5)
            {
                this.age = age;
            }
            else
            {
                Console.WriteLine("Age is Invalid");
            }

        }
        public int get_age()
        {
            return age;
        }
        public void set_grade(double grade)
        {
            if (grade>=0 &&grade<=100)
            {
                this.grade = grade;
            }
            else
            {
                Console.WriteLine("Grade is Invalid");
            }

        }
        public double get_grade()
        {
            return grade;
        }
        public void DisplayInfo()
        {
            Console.WriteLine($" Name : {name}");
            Console.WriteLine($" Age : {age}");
            Console.WriteLine($" Grade :{grade}");

        }
        public static void Main(String[] arge)
        {
            Student student = new Student("Mostafa", 3, 85);

            student.set_age(19);
            student.set_grade(85);
            student.DisplayInfo();
            //Student student1 = new Student();
            //student1.set_name("Mostafa");
            //student1.set_age(2);
            //student1.set_grade(850);
            //student1.DisplayInfo();
        }
    }
}
