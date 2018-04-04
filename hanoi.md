# python-
# 利用递归函数移动汉诺塔:
def move(n, a, b, c):
    if n == 1:
        print('move', a, '-->', c)
    else:
        move(n-1, a, c, b)
        move(1, a, b, c)
        move(n-1, b, a, c)

move(4, 'A', 'B', 'C')

主要思想是：
先把n-1层（记为+）借助c，从a移到b
再把最底下那层也就是最大的那个（记为++）借助b，从a移到c
最后再把+借助a，从b移到c
