<div align="center">

## circle


</div>

### Description

demonstrate how to make a circle with out using the provided circle command. for those of you who have ever need to make use of the symetry of a circle here's a program that will help. The code provided is made into a simple screen saver
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Psypher](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/psypher.md)
**Level**          |Intermediate
**User Rating**    |3.7 (11 globes from 3 users)
**Compatibility**  |Borland C\+\+
**Category**       |[Graphics/ Sound](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/graphics-sound__3-15.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/psypher-circle__3-333/archive/master.zip)





### Source Code

```
//by: psypher whopper
#include <stdio.h>
#include <time.h>
#include <conio.h>
#include <graphics.h>
#include <math.h>
#include <dos.h>
#include <stdlib.h>
#include <time.h>
int main(void)
{
	int gdriver = DETECT, gmode;
	double x, y, theta, r;
	int i, c, thetamax, step;
	initgraph(&gdriver, &gmode, "");
	struct palettetype pal;
	getpalette(&pal);
	for (i=0; i<pal.size; i++)
	setrgbpalette(pal.colors[i], i * 2 , 2, i*4);
	randomize();
	do {
	for (i=0; i<pal.size; i++)
	setrgbpalette(pal.colors[i], i * random(14) ,i * random(14), i * random(14));
	r = random(230) + 20;
	thetamax = random(360) + 1;
	step = random(15) + 1;
	for(theta = 0; theta <= thetamax; theta+=step)
		{
		if(kbhit())
			c = getch();
		x = cos(theta);
		y = sin(theta);
		setcolor(random(14)+ 1);
		delay(10);
		rectangle(300 + x * r, 200 + y * r, 350 + x * r, 250 + y * r);
		}
 for(theta = 0; theta <= thetamax; theta+=step)
		{
		if(kbhit())
			c = getch();
		x = cos(theta);
		y = sin(theta);
		setcolor(0);
		delay(10);
		rectangle(300 + x * r, 200 + y * r, 350 + x * r, 250 + y * r);
		}
	if(kbhit())
		c = getch();
	} while(c != 13);
	return(0);
}
```

