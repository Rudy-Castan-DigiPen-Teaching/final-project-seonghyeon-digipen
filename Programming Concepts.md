1. Shapes
Shapes are arc, circle, ellipse, line, point, quad, rect, square, triangle. Also, you can use vertex to make any shape.
This is important because it shows us what is it.
We can use it like arc(x, y, width, height, start, stop), circle(x, y, diameter), ellipse(x, y, width, height), line(x1, y1, x2, y2), point(x, y), quad(x1, y1, x2, y2, x3, y3, x4, y4), rect(x, y, width, height), square(x, y, diameter), triangle(x1, y1, x2, y2, x3, y3).
In my game, I use circle and rect to make cannon and target and button. ex) circle(0, 0, this.width);  circle(this.x,this.y,this.radius)
    circle(this.x - 10,this.y - 5,this.radius/3)
    circle(this.x + 10,this.y - 5,this.radius/3)
    push()
    fill('black');
    circle(this.x - 10 + moving,this.y - 5 + moving,this.radius/9)
    circle(this.x + 10 + moving,this.y - 5 + moving,this.radius/9)
   pop()
 rect(0, 0, this.width, this.height);

2. Colors
Colors are filling to the background and shapes. We can use color using fill() and stroke().
When we make the color, we can call a color function with 1~4 arguments or the Hexadecimal color codes or just the color names.
 This is important because it makes more fascinated to others.
In my game, I use fill() to fill the color. ex) fill('black'); background(BG1)

3. Variables 
Variables store values in memory for future use by programs. We can change the value easily while the program is running.
 This is important because we can use variables to avoid repeating ourselves in the code
We can use it let, var ,const + 'name'. In my game, I use let and const. ex) const MAIN_MENU = 1; const CREDITS_SCREEN = 2; let CannonColor = 220; let CurrentScene = MAIN_MENU;

4. Conditional Statements
Conditional statements are making the situation and responds to the situation. Like If I do this, It is happen. 
We can use it if(){} and switch(){}' if(x<0){ A = B }' ' switch(value){ case 1: A case 2: B }'
This is important because we can use these conditional statements to make the situation
In my game, I use if(){} and switch(){} ex)switch (CurrentScene) {
    case MAIN_MENU:
      background(BG1)
      MainMenuScene.Update();
      MainMenuScene.Draw();
      break;
    case CREDITS_SCREEN:
      background(BG3)
      CreditsScene.Update();
      CreditsScene.Draw();
      break;

5. Loops 
Loops are making thing again and again. In loops we have for loop and while loop. We can make the situation during the loop.
This is when we think the code line repeats, we can reduce this type of repetition to fewer lines because we can run the code line more than once using the loop.
We can use it 'for((set start value); (during value); (change value)){statement} or while(during value){statement} noLoop();'
In my game, I use for(){}. ex)  for (let i = 0; i < bullets.length; i++) {
    bullets[i].show();
    bullets[i].update();}

6. Functions 
A function is a set of statements that perform a task. Function may have a variable, and when a function is called, the variable is called.
We can use function + 'name'. This is important because we don’t have to make same things again and again.
In my game, I use function 'function Power(){} ' function Power() {
  push()
  fill('red');
  rect(10, height - 140, power1 * 1000, 20);
  pop()

  if (keyIsDown(32)) {
    if (0 < power2 && power2 <= 100) {
      power2 -= 1;
      val -= 0.001;
      power1 -= 0.001;
    }
    if (power2 <= 0) {
      power2 += 1;
      val += 0.001;
      power1 += 0.001;
    }
  }
}

7. Classes 
Class  is a template for the creation of objects. 
In class, We make constructor() to make objects and make draw() to show shape of an object and make update() to change the behavior or status of an object.
This is important because we can make new object and the behavior or status of object.
We can use 'class 'name'{ constructor(){} draw(){} update(){} }'. In my game, I use to make target and bullets and part ect.. ex)class Part{
    constructor(){
        const center_x = width / 2;
        this.part1 = new Button(center_x, height * 2/5, "part1");
        this.part2 = new Button(center_x, height * 3/5, "part2");
        this.part3 = new Button(center_x, height * 4/5, "part3");
    }

    Update(){
        if(this.part1.DidClickButton()){
          console.log("part1!");
           CurrentScene = PART1_SCREEN;
        } else if(this.part2.DidClickButton())
        {
            console.log("part2!");
            CurrentScene = PART2_SCREEN;
        } else if(this.part3.DidClickButton()){
            console.log("part3!");
            CurrentScene = PART3_SCREEN;
        }
    }
    Draw(){
        DrawTitle("Part");
        this.part1.DrawButton();
        this.part2.DrawButton();
        this.part3.DrawButton();
    }
}

8. Arrays
Array is a list of variables that have each sector and name. we can use it ' var A = [];'
This is important because it makes possible to work with more variables without creating a new name for each one.
In my game, I use array. ex) let left_bullet = [1, 2, 3, 4, 5, 6, 7] function Left_bullets() {
  for (var i = 0; i < left_bullet.length; i++) {
    var x = 20 + i * 30
    image(Cannon_Ball, x, 20, 25, 25);
    if (shot === true) {
      k += 1;
      shot = false
    }
  }
}
