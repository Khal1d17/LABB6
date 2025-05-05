import random
n = int(input("Sətir sayını daxil edin: "))
m = int(input("Sütun sayını daxil edin: "))
min_val = int(input("Minimum dəyəri daxil edin: "))
max_val = int(input("Maksimum dəyəri daxil edin: "))

A = []
for i in range(n):
    row = [] 
    for j in range(m):
        element = random.randint(min_val, max_val) 
        row.append(element)
    A.append(row)  
for i in range(n):
    row_sum = sum(A[i]) 
    if row_sum > 0:  
        print(f"Müsbət cəmi olan ilk satırın nömrəsi: {i + 1}")
        break
else:
    print("Heç bir müsbət cəm tapılmadı.")
