# Bài soạn python về Tuples, Sets, Dictionaries
## 1. Tuples

### Python Tuple
#### - Tuple
Tuple được sử dụng để lưu trữ nhiều mục trong một biến duy nhất.
Một tuple là một tập hợp được sắp xếp và 'không thể thay đổi'.
Các tuple được viết bằng dấu ngoặc tròn.
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
print(thistuple)
```

</details>

#### - Tuple Items
Các mục tuple được sắp xếp theo thứ tự, không thể thay đổi và cho phép các giá trị trùng lặp.
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry", "apple", "cherry")
print(thistuple)

```
</details>

#### - Tuple With One Item
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

#### - Tuple Data Types
Các mục tuple có thể thuộc bất kỳ kiểu dữ liệu nào:
<details>
  
```shell script
tuple1 = ("abc", 34, True, 40, "male")
```

</details>

#### - Tuple() Constructor
Có thể sử dụng hàm tạo tuple() để tạo một tuple.
<details>
  
```shell script
thistuple = tuple(("apple", "banana", "cherry")) # note the double round-brackets
print(thistuple)
```

</details>

### Access Tuple
#### - Access Tuple Items
Truy cập các mục tuple bằng cách tham chiếu đến số chỉ mục, bên trong dấu ngoặc vuông:
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
print(thistuple[1])
```

</details>

#### - Negative Indexing
Lập chỉ mục âm có nghĩa là bắt đầu từ cuối.
-1đề cập đến mục cuối cùng, -2đề cập đến mục thứ hai từ cuối, v.v.
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
print(thistuple[-1])
```

</details>

#### - Range of Indexes
Chỉ định một phạm vi chỉ mục bằng cách chỉ định nơi bắt đầu và nơi kết thúc phạm vi.
Ví dụ trả về mục thứ ba, thứ tư và thứ năm:
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[2:5])
```

</details>

#### - Check if Item Exists
Xác định xem một mục cụ thể có xuất hiện trong một bộ hay không
Ví dụ kiểm tra xem "apple" có trong tuple không
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
if "apple" in thistuple:
  print("Yes, 'apple' is in the fruits tuple")
```

</details>









