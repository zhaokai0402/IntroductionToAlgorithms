# 循环不变式
循环不变式：对于每次循环，子数组中（已选择的元素）已排序。

初始化：在第一次循环前（j = 1）时，子数组中不包含元素，故是已排序的。

保持：从A[j]..A[n]中选出最小数与A[j]交换，因此A[1] < A[2] <..A[j - 1] < A[j]。循环不变式保持。

结束：当j = n - 1 时，A[n - 1]必然小于A[n](由保持可得)，故A[0]..A[n]都是有序的。算法成立


# 对前n-1数排序
由保持的性质可值，当j = n - 1 时 从A[n - 1]和A[n] 中选出最小数和A[n - 1] 交换， 因此 A[n - 1] < A[n]。故不需要对前n-1数执行即可。

# 最好情况和最坏情况
最好：n^2 + 3n - 4  最坏：1.5n^2 + 2.5n - 4