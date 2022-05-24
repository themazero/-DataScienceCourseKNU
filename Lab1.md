1. . Створити змінні базових (atomic) типів. Базові типи: character, numeric, 
integer, complex, logical:
s <- "KNUCA"
x <- 2L
y <- 2.0
a <- 1 + 4i
b <- FALSE
2. Створити вектори, які: містить послідовність з 5 до 75: 
v_1 <- 5:75
v_2 <- c(3.14,2.71,0,13)
v_3 <- c(rep(x = TRUE, times = 100))
3. Створити наступну матрицю за допомогою matrix, :
mat2 <- matrix(c(0.5, 1.3, 3.5, 3.9, 131, 2.8, 0, 2.2, 4.6, 2, 7, 5.1), nrow = 4, ncol = 3, byrow = TRUE)
результат:
> mat2
     [,1]  [,2] [,3]
[1,]  0.5   1.3  3.5
[2,]  3.9 131.0  2.8
[3,]  0.0   2.2  4.6
[4,]  2.0   7.0  5.1
> 
та за допомогою cbindабо rbind:
r1 <- c(0.5,1.3,3.5)
r2 <- c(3.9,131, 2.8)
r3 <- c(0, 2.2, 4.6)
r4 <- c(2, 7, 5.1)
mat1 <- rbind(r1, r2, r3, r4)
результат:
> mat1
   [,1]  [,2] [,3]
r1  0.5   1.3  3.5
r2  3.9 131.0  2.8
r3  0.0   2.2  4.6
r4  2.0   7.0  5.1
> 

4. Створити довільний список (list), в який включити всі базові типи.:
list_data<- list("FAIT", c(21,32,11), TRUE, 51.23, 2+3i,3L)
5. Створити фактор з трьома рівнями «baby», «child», «adult».:
f <- factor(c("baby", "child", "adult", "child", "baby", "adult"), 
            levels = c("baby", "child", "adult"))
6. Знайти індекс першого значення NA в векторі 1, 2, 3, 4, NA, 6, 7, NA, 9, NA, 11. 
v_4 <- c(1, 2, 3, 4, NA, 6, 7, NA, 9, NA, 11) :
match(c(NA),v_4)
результат:
> match(c(NA),v_4)
[1] 5
> 
Знайти кількість значень NA.:
sum(is.na(v_4))
результат:
> sum(is.na(v_4))
[1] 3
> 
7. Створити довільний data frame та вивести в консоль.:
name <- c("Ihor","Mykola","Nazar","Maksym","Anatoliy")
age <- c(22,32,24,54,20)
city <- c("Kyiv","Kharkiv","Lviv","Odesa","Dnipro")
peoples <- data.frame(Name = name, Age = age, City = city)
print(peoples)
результат:
8. Змінити імена стовпців цього data frame.:
names(peoples) <- c('FirstName', 'Years', 'PlaceofBi')
print(peoples)
 FirstName Years PlaceofBirdh
1      Ihor    22         Kyiv
2    Mykola    32      Kharkiv
3     Nazar    24         Lviv
4    Maksym    54        Odesa
5  Anatoliy    20       Dnipro
> 
