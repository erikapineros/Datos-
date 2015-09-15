String meses[] = {"enero", "febrero", "marzo","abril", "mayo", "junio", "Julio","agosto", "septiembre","Octubre","Noviembre","diciembre", };

int numeros[] = {100,0,120,200,270,320,440,500,600,270,455};

PFont gluck;




void setup () {
  size (840,440);
  gluck = loadFont("GandhiSans-Bold-24.vlw");
  textFont(gluck,28);
  }
  
  
void draw(){
  background (0); 
  
  //arboles
  fill (80,78,70);
  rect(95, 260, 7, 70);
  rect(115, 280, 7, 50);
  rect(65, 260, 7, 90);
  rect(155, 270, 7, 50);
  fill (170,200,50);
   ellipse(100, 260, 20, 20);
   ellipse(70, 270, 20, 20);
   ellipse(160, 280, 20, 20);
   ellipse(120, 280, 20, 20);
   
   
   // letrero
  fill (170,200,50);
  rect(30, 320, 750, 70);
  fill (95,95,80);
  text("TALA DE ARBOLES 2014", 270,365);
   text("Arboles talados", 260,300);
   text("Arbustos perdidos",490,300);
   text("Datos por hectarias",540,420);
  
  //datos
  for (int YY = 0; YY < 12; YY=YY +2){
     text (meses[YY], 10,20 + (YY * 20));
   
   //datos arboles talados
     fill (18,177,44);
     rect (160, (YY*20), numeros[YY], 24 );
     rect(450, 280, 20, 20);
    
     //datos arbustos perdidos
     fill (100);
    rect (160, (YY*20), numeros[YY], 10 );
    rect(720, 280, 20, 20);
     
     text (numeros [YY], 180 + numeros [YY],  25 + (YY * 20));
     
  }
}
