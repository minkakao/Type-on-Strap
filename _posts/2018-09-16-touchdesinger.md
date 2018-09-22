---
layout: post
title: Processing talking to Touchdesigner
feature-img: "assets/img/pexels/touchd1.jpg"
thumbnail: "assets/img/thumbnails/touchd1.jpg"
tags: [Test, Lorem]
---

How to connect Processing and TouchDesinger 

1. Open Processing library
2. Add two libraries "Spout for Processing" and "Syphon" 
3. Comback to your processing sketch
4. write the following code before setup: 
    import codeanticode.syphon.*;
    import spout.*;
    String sendername; 
    Spout spout;
    
5. in setup, write the following code
void setup()  { 
  spout = new Spout(this);
  sendername = "littleprince";
  spout.createSender(sendername, width, height);
}
6. in draw function, wrtie the following code at the very last:
void draw()  { 
  spout.sendTexture();
  }
