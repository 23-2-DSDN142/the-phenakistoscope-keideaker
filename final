const SLICE_COUNT = 9;

function setup_pScope(pScope){
  pScope.output_mode(ANIMATED_DISK);
  pScope.scale_for_screen(true);
  pScope.draw_layer_boundaries(false);
  pScope.set_direction(CW);
  pScope.set_slice_count(SLICE_COUNT);
  pScope.load_image("whiteflower" , "png");
  pScope.load_image("flowerleaf" , "png");
  pScope.load_image("flowerleaf2" , "png");
  pScope.load_image("flowerleaf3" , "png");
  pScope.load_image("flowerleaf4" , "png");
  pScope.load_image("pinkflower" , "png");

}

function setup_layers(pScope){
//10 layers in total
  new PLayer(null,"#fa97a9"); //lets us draw the whole circle background, ignoring the boundaries
 
  var layer8 = new PLayer(darkpinkcircle);
  layer8.mode( RING );
  layer8.set_boundary( 0, 400 );

  var layer9 = new PLayer(darkpinkcircle);
  layer9.mode( RING );
  layer9.set_boundary( 0, 400 );

  var layer10 = new PLayer(circles3);
  layer10.mode( RING );
  layer10.set_boundary( 0, 400 );

  var layer1 = new PLayer(circles2);
  layer1.mode(RING);
  layer1.set_boundary( 0, 800 );

  var layer1 = new PLayer(circles);
  layer1.mode(RING);
  layer1.set_boundary( 0, 800 );

  var layer1 = new PLayer(whiteflower);
  layer1.mode(SWIRL(0.5));
  layer1.set_boundary( 100, 170 );

  var layer2 = new PLayer(flowerleaf);
  layer2.mode(SWIRL(1));
  layer2.set_boundary( 700, 750 );
  
  var layer3 = new PLayer (flowerleaf2);
  layer3.mode(SWIRL(1));
  layer3.set_boundary( 520,600)

  var layer4 = new PLayer (flowerleaf3);
  layer4.mode(SWIRL(1));
  layer4.set_boundary( 500, 600)

  var layer5 = new PLayer (flowerleaf4);
  layer5.mode(SWIRL(1));
  layer5.set_boundary( 550 ,600)

  var layer6 = new PLayer(frontflower);
  layer6.mode(RING);
  layer6.set_boundary( 200, 1000 );

  //var layer7 = new PLayer(pinkflower)
  //layer7.mode( RING )
  //layer7.set_boundary( 0 , 300)


}


function whiteflower(x, y, animation, pScope){
  scale(1)
  translate(0, 0);
  scale(animation.frame*1);
  pScope.draw_image("whiteflower",100,-130)
}
//dark pink circle
function darkpinkcircle(x, y, animation, pScope){

  let angleOffset = (360 / SLICE_COUNT) / 2
  let backgroundArcStart = 270 - angleOffset;
  let backgroundArcEnd = 270 + angleOffset;

  fill("#d33c3f")
  arc(x,y,1600,1600,backgroundArcStart,backgroundArcEnd);
}

function lightpinkcircle(x, y, animation, pScope){
//lighter pink circle
  let angleOffset = (360 / SLICE_COUNT) / 2
  let backgroundArcStart = 270 - angleOffset;
  let backgroundArcEnd = 270 + angleOffset;

  fill("#ec9ba9")
  arc(x,y,1550,1550,backgroundArcStart,backgroundArcEnd);
}

//all flowerleafs are the outer circle
function flowerleaf(x, y, animation, pScope){
  scale(0.5)
  pScope.draw_image("flowerleaf",x,-300)
}

function flowerleaf2(x, y, animation, pScope){
  scale(0.5)
  pScope.draw_image("flowerleaf2",300,-650)
}

function flowerleaf3(x, y, animation, pScope){
  scale(0.5)
  pScope.draw_image("flowerleaf3",600,-600)
}

function flowerleaf4(x, y, animation, pScope){
  scale(0.5)
  pScope.draw_image("flowerleaf4",-300,-570)
}
//middle pink circle
function frontflower(x, y, animation, pScope){
 
  let angleOffset = (360 / SLICE_COUNT) / 2
  let backgroundArcStart = 270 - angleOffset;
  let backgroundArcEnd = 270 + angleOffset;
  strokeWeight(0)
  fill("#e26270")
  arc(x,y,400,400,backgroundArcStart,backgroundArcEnd);
}

//function pinkflower(x, y, animation, pScope){
  //scale(0.2)
  //pScope.draw_image("pinkflower",0,600)


//yellow petals
function circles(x, y, animation, pScope){

  fill("#f5cb6a")
  strokeWeight(0)
  let ballSize  = 300 + (animation.wave(1)* 20)
  let bounce = 50* animation.wave()
  ellipse(0, 250+bounce ,ballSize); 
}
//grene petal
function circles2(x, y, animation, pScope){

  fill("#939a3c")
  strokeWeight(0)
  let ballSize  = 600 + (animation.wave(1)* 20)
  let bounce = 50* animation.wave()
  ellipse(0, 250+bounce ,ballSize); 
}
//darkgreen circle
function circles3(x, y, animation, pScope){

  let angleOffset = (360 / SLICE_COUNT) / 2
  let backgroundArcStart = 270 - angleOffset;
  let backgroundArcEnd = 270 + angleOffset;
  fill("#384e33")
  arc(x,y,1400,1400,backgroundArcStart,backgroundArcEnd);
}
