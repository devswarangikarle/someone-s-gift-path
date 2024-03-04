# someone-s-gift-path
 an n*m grid and the gift is located at {k, l},  string that contains characters {L, R, D, U},  tell whether he will reach {k, l}. L , R , U  and D . Assuming (x, y) is the initial point, here's how L, R, D, and U works in a grid: L : moves to (x-1, y) R : moves to (x+1, y) D : moves to (x, y-1) U : moves to (x, y+1)

def will_reach_gift(k, l, path):
    x, y = 0, 0
    for move in path:
        if move == 'L':
            x -= 1
        elif move == 'R':
            x += 1
        elif move == 'D':
            y -= 1
        elif move == 'U':
            y += 1

        if x == k and y == l:
            return "YES"

    return "NO"

k, l = map(int, input().split())
path = input().strip()


result = will_reach_gift(k, l, path)
print(result)
