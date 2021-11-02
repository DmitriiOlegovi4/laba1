using System.Collections.Generic;

using System.Linq;

using System.Text;

using cod;

namespace cod

{

public class Student : Human

{

    private string faculty = "";

    private short course=1;

    private short average_score=0;

    private short[] score=new short[5];

    

      

     public Student(){}

     public Student(short age, short height_cen,short

     course, short number,string

     name,string faculty,string street,string surname )

    {

    	

    	Random rand=new Random();

    	address.number = number;

        address.street = street;

        this.surname=surname;

       for(short i=0;i<5;i++){

       	

       	score[i]=Convert.ToInt16(rand.Next(1,6));

       	

       }

       

       this.age = age;

        this.height_cen = height_cen;

        this.course = course;

        this.name = name;

        this.faculty = faculty;

    }

    

    

     	

   /* public short Score{

     	

     	set { 

     		

     		short []kistul=new short[score.Length+1];

     		for(short i=0;i<score.Length;i++){

     			

     			kistul[i]=score[i];

     			

     		}

     		

     		kistul[score.Length]=value;

     		

          score=kistul;

     	

     	}

     }*/

     

   public  short Age

     {

         set {age = value;}

         get{return age;}

     }

   public  short Height_cen

     {

         set { height_cen = value; }

         get { return height_cen; }

     }

    public short Course

     {

         set { course = value; }

         get { return course; }

     }

   public  string Name

     {

         set { name = value; }

         get { return name; }

     }

    public string Surname

    {

        set { surname = value; }

        get { return surname; }

    }

   public  string Faculty

     {

         set { faculty = value; }

         get { return faculty; }

     }

    public int Average_score

     {

        // set { average_score = value; }

         get { 

         	for(short i=0;i<score.Length;i++)

         	{

         		

         		average_score+=score[i];

         		

         	}

         	

         	return average_score/score.Length;

         	

         	}

         	

     }

         public short Number

    {

        set { address. number= value; }

        get { return address.number; }

    }

   public string Street

    {

        set { address.street = value; }

        get { return address.street; }

    }

    

    

		public void	Get_Score(){ 



     	for(short i=0;i<score.Length;i++){ 



     	  Console.WriteLine(score[i]);

     	 }

     	}

     	

     	

     	  public void	Get_student_type(){ 

         switch(Average_score){

         	

         	case 3:

         	Console.WriteLine("C grade");

         	break;

         	

         	case 4:

         	Console.WriteLine("B grade");

         	break;

         	

         	case 5:

         	Console.WriteLine("A grade");

         	break;

         	

         	default:

         	Console.WriteLine("F grade");

         	break;

         	

         	

         }

         }

     	

}
}
