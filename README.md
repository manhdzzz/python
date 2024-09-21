## Bài soạn python về Tuples, Sets, Dictionaries
### 1. Tuples

#### Tuple
Tuple được sử dụng để lưu trữ nhiều mục trong một biến duy nhất.
Một tuple là một tập hợp được sắp xếp và 'không thể thay đổi'.
Các tuple được viết bằng dấu ngoặc tròn.
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
print(thistuple)
```

</details>
#### Tuple Items
Các mục tuple được sắp xếp theo thứ tự, không thể thay đổi và cho phép các giá trị trùng lặp.
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry", "apple", "cherry")
print(thistuple)

```
</details>
#### Tuple With One Item
Để tạo một tuple chỉ có một phần tử, phải thêm dấu phẩy sau phần tử đó, nếu không Python sẽ không nhận dạng được đó là một tuple.
<details>
  
```shell script
thistuple = ("apple",)
print(type(thistuple))
//NOT a tuple
thistuple = ("apple")
print(type(thistuple))
```

</details>



