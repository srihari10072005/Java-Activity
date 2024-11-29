abstractclassShape{
//Abstractmethodstobeimplementedbysubclasses
public abstract double calculateArea();
publicabstractdoublecalculatePerimeter();
}
classCircleextendsShape{
private double radius;
// Constructor for Circle
publicCircle(doubleradius){
this.radius=radius;
}
@Override
public double calculateArea() {
returnMath.PI*radius*radius;
}
@Override
publicdoublecalculatePerimeter(){
return 2 * Math.PI * radius;
}
}
classTriangleextendsShape{
private double side1;private
double side2;private double
side3;
//ConstructorforTriangle
publicTriangle(doubleside1,doubleside2,doubleside3){ this.side1
= side1; 
this.side2=side2;
this.side3=side3;
}
@Override
publicdoublecalculateArea(){
//UsingHeron'sformulatocalculateareaofatriangle double s =
(side1 + side2 + side3) / 2;
returnMath.sqrt(s*(s-side1)*(s -side2)*(s- side3));
}
@Override
publicdoublecalculatePerimeter(){
return side1 + side2 + side3;
}
}
publicclassMain{
publicstaticvoidmain(String[]args){
//CreatinginstancesofCircleandTriangle Circle
circle = new Circle(5);
Triangletriangle=newTriangle(3,4, 5);
// Calculating and displaying area and perimeter for Circle
System.out.println("Circle - Area: " + circle.calculateArea());
System.out.println("Circle-Perimeter:"+circle.calculatePerimeter());
// Calculating and displaying area and perimeter for Triangle
System.out.println("Triangle - Area: " + triangle.calculateArea());
System.out.println("Triangle-Perimeter:"+triangle.calculatePerimeter());
}
}
