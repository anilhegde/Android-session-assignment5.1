public class Assignment51 {

	public static void main(String[] args) {
		Circle c = new Circle (2);
		c.findArea();
		c.findPerimeter();
		System.out.println(c);
		
		Rectangle r = new Rectangle (2.5,10);
		r.findArea();
		r.findPerimeter();
		System.out.println(r);
		
		Triangle t = new Triangle(2, 3, 4, 6);
		t.findArea();
		t.findPerimeter();
		System.out.println(t);

	}

}

abstract class Figure{
	protected double d1;
	abstract void findArea();
	abstract void findPerimeter();
}

class Circle extends Figure{
	double area, peri;
	Circle(double r){
		d1=r;
	}
	void findArea(){
		area=3.14*d1*d1;
	}
	void findPerimeter(){
		peri=2*3.14*d1;
	}
	@Override
	public String toString() {
		return "Circle [area=" + area + ", peri=" + peri + "]";
	}
	
	
}

class Rectangle extends Figure{
	double area, peri,d2;
	Rectangle(double x, double y){
		d1=x;
		d2=y;
	}
	void findPerimeter(){
		peri=2*(d1+d2);
	}
	@Override
	void findArea() {
		area=d1*d2;
		
	}
	@Override
	public String toString() {
		return "Rectangle [area=" + area + ", peri=" + peri + "]";
	}
	
}

class Triangle extends Figure{
	double area, peri, h,a,c;
	Triangle(double b, double h,double a, double c){
		d1=b;
		this.h=h;
		this.a=a;
		this.c=c;
	}
	void findArea(){
		area=h*d1/2;
	}
	void findPerimeter(){
		peri=a+d1+c;
	}
	@Override
	public String toString() {
		return "Triangle [area=" + area + ", peri=" + peri + "]";
	}
	
	
}
