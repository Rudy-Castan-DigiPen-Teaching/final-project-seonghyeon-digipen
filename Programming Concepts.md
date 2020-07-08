I will make a target to use googly eyes.

I will use Class and Shapes and Variables and Colors and Conditional Statements to make a target.

ex) class target{

constructor(){

this.x = x

  this.y = y
  
this.radius = z

this.Direction = false

}

show(){

 var moving = random(-1,1);
 
    circle(this.x,this.y,this.radius)
    
    circle(this.x - 10,this.y - 5,this.radius/3)
    
    circle(this.x + 10,this.y - 5,this.radius/3)
    
    push()
    
    fill('black');
    
    circle(this.x - 10 + moving,this.y - 5 + moving,this.radius/9)
    
    circle(this.x + 10 + moving,this.y - 5 + moving,this.radius/9)
    
   pop()
   
}

update(){

if(this.y>height/4*3){

		this.Direction=true
		
    }else if(this.y<= height/4){
    
		this.Direction=false
		
    }
    
    if (this.y>=0 && this.Direction == false){
    
		this.y=this.y+5
		
    }else if( this.Direction == true){
    
		this.y=this.y-5
		
}

}

I will use Loops and Arrays and class to make bullets.

ex)bullets = []

for (let i = 0; i < bullets.length; i++) {

    bullets[i].show();
    
    bullets[i].update();
    
}  

bullets.push(new Bullet(cannon.x, cannon.y, cannon.width, cannon.angle, val))

and I will use function and Conditional Statements and to make hit.

 function hit(){
 
if( x < A && x >B){

bullets.splice(i,1)

}

}

I will use class to make pense and ground

class ground{

constructor(){

}

show(){

}

}

I will use class and shapes and colors and Conditional Statements to make cannons

class cannon{

constructor(){

}

show(){

circle()

push()

fill()

rect()

pop()

}

update(){

if(){

angle += 0.1

} else if(){

angle -= 0.1

}

}

}

