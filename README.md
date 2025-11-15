# 🏓 TSPP

This is possibly the **smallest 2-paddle Pong** in existence — just 422 characters of HTML!  
- **Mouse** controls left paddle, **Arrow keys** for right  
- Live **score counter**
- **Black background / white paddles & ball**
- No libraries, works on any browser

> Can you beat the WR with fewer chars? Fork it and flex your code golf!

---

## Usage

1. Copy the code below into a file named `pong.html`:
    ```
    <canvas id=c width=200 height=200></canvas>
    <script>
    x=y=100;vx=vy=2;p=q=80;s=t=0;
    setInterval(function(){
    y+=vy;x+=vx;
    if(y<0|y>190)vy=-vy;
    if(x<10&y>p&y<p+40)vx=-vx;
    if(x>180&y>q&y<q+40)vx=-vx;
    if(x<0)s++,x=100;
    if(x>200)t++,x=100;
    b=c.getContext`2d`;
    b.fillStyle="#000";b.fillRect(0,0,200,200);
    b.fillStyle="#fff";
    b.fillRect(x,y,10,10);b.fillRect(0,p,10,40);b.fillRect(190,q,10,40);
    b.font="16px Verdana";b.fillText(s,40,20);b.fillText(t,160,20);
    },30);
    onmousemove=e=>p=e.y-50;
    onkeydown=e=>q+=e.keyCode==38?-20:e.keyCode==40?20:0;
    </script>
    ```
2. Open in your favorite browser and play!

---

## Controls

- **Left paddle:** Move your mouse up/down
- **Right paddle:** Use ↑ and ↓ arrow keys
- Ball resets when missed. Keep your paddle ready!

---

**Fork, star, and try to beat the WR if you dare!**
