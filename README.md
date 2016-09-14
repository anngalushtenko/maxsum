# maxsum
Начиная с вершины треугольника и перемещаясь вниз на смежные числа, найдите максимальную сумму пути от вершины до основания следующего треугольника

// рекурсивная функция 

int maxsum (triangle, row=0, column=0, total=0)
{ 
if row == len(triangle) - 1:
        return total + triangle[row][column];
else
    return max(maxSum (triangle, row + 1, column, total + triangle[row][column]),
               maxSum (triangle, row + 1, column + 1, total + triangle[row][column]));
