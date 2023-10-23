# SemanaTec2-23-Oct-2023
## Act 1 Github 
### Dana Sanchez A01723361
### Sem2 ITC
### Javier Lugo
**bold Semana Tec 12** 

*italicized Desayunos*

~~The world is flat.~~

1. Hot-Cakes 🥞
2. Tacos 🌮
3. Chilaquiles 🥫
4. Galletas 🍪
5. Huevo 🍳


- Piano
- Guitarra
- Bateria
- Violin
- Flauta
---

![Paint](https://grantjenks.com/docs/freegames/_static/paint.gif)
![Día del Médico](https://tse2.mm.bing.net/th?id=OIP.u-aXmRnnLZG2LX4HrOCGBgHaEF&pid=Api&P=0&h=180)

"""Paint, for drawing shapes.

Exercises

1. Add a color.
2. Complete circle.
3. Complete rectangle.
4. Complete triangle.
5. Add width parameter.
"""

from turtle import *

from freegames import vector


def line(start, end):
    """Draw line from start to end."""
    up()
    goto(start.x, start.y)
    down()
    goto(end.x, end.y)


def square(start, end):
    """Draw square from start to end."""
    up()
    goto(start.x, start.y)
    down()
    begin_fill()

    for count in range(4):
        forward(end.x - start.x)
        left(90)

    end_fill()


def circle(start, end):
    """Draw circle from start to end."""
    pass  # TODO


def rectangle(start, end):
    """Draw rectangle from start to end."""
    pass  # TODO


def triangle(start, end):
    """Draw triangle from start to end."""
    pass  # TODO


def tap(x, y):
    """Store starting point or draw shape."""
    start = state['start']

    if start is None:
        state['start'] = vector(x, y)
    else:
        shape = state['shape']
        end = vector(x, y)
        shape(start, end)
        state['start'] = None


def store(key, value):
    """Store value in state at key."""
    state[key] = value


state = {'start': None, 'shape': line}
setup(420, 420, 370, 0)
onscreenclick(tap)
listen()
onkey(undo, 'u')
onkey(lambda: color('black'), 'K')
onkey(lambda: color('white'), 'W')
onkey(lambda: color('green'), 'G')
onkey(lambda: color('blue'), 'B')
onkey(lambda: color('red'), 'R')
onkey(lambda: store('shape', line), 'l')
onkey(lambda: store('shape', square), 's')
onkey(lambda: store('shape', circle), 'c')
onkey(lambda: store('shape', rectangle), 'r')
onkey(lambda: store('shape', triangle), 't')
done()
...
---


[Link a Markdown](https://www.markdownguide.org/cheat-sheet/)

| Nombre | Actividad |
| ----------- | ----------- |
| Dana | Trabajo a hacer |
| Dana | Trabajo a hacer |

- [x] Dana, hacer trabajo
- [ ] Dana, hacer código
- [ ] Dana,, subir tarea
