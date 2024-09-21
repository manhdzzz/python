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

#### - Tuple Items - Data Types
Theo quan điểm của Python, các bộ được định nghĩa là các đối tượng có kiểu dữ liệu 'tuple'

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
Xác định xem một mục cụ thể có xuất hiện trong một sets hay không

Ví dụ kiểm tra xem "apple" có trong tuple không
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
if "apple" in thistuple:
  print("Yes, 'apple' is in the fruits tuple")
```

</details>
### Update Tuples
Tuple không thể thay đổi, nghĩa là bạn không thể thay đổi, thêm hoặc xóa các mục sau khi tuple được tạo.

Nhưng vẫn có một số giải pháp khắc phục.
#### - Change Tuple Values
Tuple không thể thay đổi hoặc không thể thay đổi như tên gọi của nó.

Nhưng có một giải pháp thay thế. 

Ta có thể chuyển đổi tuple thành danh sách, thay đổi danh sách và chuyển đổi danh sách trở lại thành tuple.

Ví dụ chuyển đổi tuple thành danh sách để có thể thay đổi nó:
<details>
  
```shell script
x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)

print(x)
```

</details>
#### - Add Items
Vì tuple không thể thay đổi nên chúng không có phương thức tích hợp append(), nhưng vẫn có những cách khác để thêm các mục vào tuple.

+) Chuyển đổi thành danh sách

Ví dụ chuyển đổi tuple thành một danh sách, thêm "orange" và chuyển đổi nó trở lại thành tuple:
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.append("orange")
thistuple = tuple(y)
```

</details>

+) Thêm tuple vào tuple

Ví dụ tạo một tuple mới với giá trị "orange" và thêm tuple đó vào:
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
y = ("orange",)
thistuple += y

print(thistuple)
```

</details>
#### - Remove Items
Tuple không thể thay đổi! Nhưng ta có thể sử dụng giải pháp thay thế tương tự như trên để thay đổi và thêm các mục tuple:

Ví dụ chuyển đổi tuple thành một danh sách, xóa "apple" và chuyển đổi nó trở lại thành tuple:
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.remove("apple")
thistuple = tuple(y)
```

</details>
Hoặc ta có thể xóa hoàn toàn sets dữ liệu:
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
del thistuple
print(thistuple)
```

</details>
### Unpack Tuples
#### - Unpacking a Tuple
Khi chúng ta tạo một tuple, chúng ta thường gán giá trị cho nó. Điều này được gọi là "đóng gói" một tuple

Nhưng trong Python, chúng ta cũng được phép trích xuất các giá trị trở lại thành các biến. Điều này được gọi là "giải nén"

Ví dụ giải nén:
<details>
  
```shell script
fruits = ("apple", "banana", "cherry")

(green, yellow, red) = fruits

print(green)
print(yellow)
print(red)
```

</details>
#### - Using Asterisk *
Nếu số biến ít hơn số giá trị, ta có thể thêm một dấu * vào tên biến và các giá trị sẽ được gán cho biến dưới dạng danh sách:

Ví dụ gán phần giá trị còn lại dưới dạng danh sách có tên là "đỏ":
<details>
  
```shell script
fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")

(green, yellow, *red) = fruits

print(green)
print(yellow)
print(red)
```

</details>
### Python - Loop Tuples
#### - Loop Through a Tuple
Lặp qua các mục của tuple bằng cách sử dụng for vòng lặp.
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
for i in range(len(thistuple)):
  print(thistuple[i])
```

</details>
Lặp qua các mục của tuple bằng cách sử dụng while vòng lặp.
<details>
  
```shell script
thistuple = ("apple", "banana", "cherry")
i = 0
while i < len(thistuple):
  print(thistuple[i])
  i = i + 1
```

</details>
### Python - Join Tuples
#### - Join Two Tuples
Để nối hai hoặc nhiều cặp, ta có thể sử dụng toán tử +
<details>
  
```shell script
tuple1 = ("a", "b" , "c")
tuple2 = (1, 2, 3)

tuple3 = tuple1 + tuple2
print(tuple3)
```

</details>
#### - Multiply Tuples
Nhân nội dung của một tuple với số lần nhất định, ta có thể sử dụng toán tử *
<details>
  
```shell script
fruits = ("apple", "banana", "cherry")
mytuple = fruits * 2

print(mytuple)
```

</details>


## 2. Sets
### Python Sets
Một tập hợp là một tập hợp không được sắp xếp , không thể thay đổi * và không được lập chỉ mục .

Ví dụ
<details>
  
```shell script
thisset = {"apple", "banana", "cherry"}
print(thisset)
```

</details>
#### - Set Items
Các mục thiết lập không được sắp xếp, không thể thay đổi và không cho phép giá trị trùng lặp.
### Unordered
Không có thứ tự có nghĩa là các mục trong một tập hợp không có thứ tự xác định.

Các mục thiết lập có thể xuất hiện theo thứ tự khác nhau mỗi khi bạn sử dụng chúng và không thể được tham chiếu bằng chỉ mục hoặc khóa.
#### - Unchangeable
Các mục trong sets không thể thay đổi, nghĩa là chúng ta không thể thay đổi các mục sau khi sets đã được tạo.
#### - Duplicates Not Allowed
Một sets không thể có hai phần tử có cùng giá trị.

Các giá trị trùng lặp sẽ bị bỏ qua:
<details>
  
```shell script
thisset = {"apple", "banana", "cherry", "apple"}

print(thisset)
```

</details>
True và 1được coi là có cùng giá trị:
<details>
  
```shell script
thisset = {"apple", "banana", "cherry", True, 1, 2}

print(thisset)
```

</details>
Tương tự với False và 0.

### Set Items - Data Types
Tương tự như Tuples

Theo quan điểm của Python, tập hợp được định nghĩa là các đối tượng có kiểu dữ liệu là 'set'
### Add Set Items
#### - Add Items
Sau khi tạo xong một sets, ta không thể thay đổi các mục trong sets đó nhưng có thể thêm các mục mới.
Để thêm một mục vào tập hợp, ta sử dụng add()
<details>
  
```shell script
thisset = {"apple", "banana", "cherry"}

thisset.add("orange")

print(thisset)
```

</details>
#### - Add Sets
Để thêm các mục từ tập hợp khác vào tập hợp hiện tại, ta sử dụng update()
<details>
  
```shell script
thisset = {"apple", "banana", "cherry"}
tropical = {"pineapple", "mango", "papaya"}

thisset.update(tropical)

print(thisset)
```

</details>
#### - Add Any Iterable
<details>
  
```shell script
thisset = {"apple", "banana", "cherry"}
mylist = ["kiwi", "orange"]

thisset.update(mylist)

print(thisset)
```

</details>
### Remove Set Items
#### - Remove Item
Để xóa một mục trong một tập hợp, ta sử dụng phương thức remove(), discard(), pop(), clear() hoặc del.
<details>
  
```shell script
thisset = {"apple", "banana", "cherry"}
thisset.remove("banana") // Nếu mục cần xóa không tồn tại, remove() sẽ xảy ra lỗi.
print(thisset)

//hoặc

thisset = {"apple", "banana", "cherry"}
thisset.discard("banana") // Nếu mục cần xóa không tồn tại thì discard() sẽ KHÔNG xảy ra lỗi.
print(thisset)

//hoặc xóa một mục ngẫu nhiên bằng cách sử dụng pop()

thisset = {"apple", "banana", "cherry"}
x = thisset.pop()
print(x)
print(thisset)

//hoặc clear() làm rỗng tập hợp

thisset = {"apple", "banana", "cherry"}
thisset.clear()
print(thisset)

//hoặc xóa toàn sets tập hợp
thisset = {"apple", "banana", "cherry"}
del thisset
print(thisset)
```

</details>
### Python - Join Sets
#### - Join Sets
Có một số cách để nối hai hoặc nhiều tập hợp trong Python:

Các phương thức union() và update() nối tất cả các mục từ cả hai tập hợp.

Phương pháp intersection() chỉ giữ lại các bản sao.

Phương pháp difference() giữ lại các phần tử từ tập đầu tiên không có trong tập khác.

Phương pháp symmetric_difference() giữ lại tất cả các mục trừ các mục trùng lặp.
#### - Union
Nối set1 và set2 thành một set mới
<details>
  
```shell script
set1 = {"a", "b", "c"}
set2 = {1, 2, 3}
set3 = set1.union(set2)
print(set3)
```

</details>
Nối một set với một tuple
<details>
  
```shell script
x = {"a", "b", "c"}
y = (1, 2, 3)
z = x.union(y)
print(z)
```

</details>
#### - Update
Phương pháp update() chèn các mục trong set2 vào set1:
<details>
  
```shell script
set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}
set1.update(set2)
print(set1)
```

</details>
#### - Intersection
Nối set1 và set2 nhưng chỉ giữ lại các phần tử trùng lặp
<details>
  
```shell script
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set3 = set1.intersection(set2)
print(set3)
```

</details>
Phương pháp intersection_update() CHỈ giữ lại các phần tử trùng lặp, nhưng nó sẽ thay đổi tập hợp gốc thay vì trả về một tập hợp mới
<details>
  
```shell script
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set1.intersection_update(set2)
print(set1)
```

</details>
#### - Difference
Giữ lại tất cả các mục từ set1 không có trong set2
<details>
  
```shell script
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set3 = set1.difference(set2)
print(set3)
```

</details>
Ta có thể sử dụng toán tử '-' thay cho difference() và bạn sẽ nhận được kết quả tương tự
<details>
  
```shell script
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set3 = set1 - set2
print(set3)
```

</details>
Phương pháp difference_update() cũng sẽ giữ lại các phần tử từ tập đầu tiên không có trong tập khác, nhưng nó sẽ thay đổi tập ban đầu thay vì trả về một tập mới.
<details>
  
```shell script
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set1.difference_update(set2)
print(set1)
```

</details>
#### - Symmetric Differences
Giữ lại những vật phẩm không có trong cả hai sets
<details>
  
```shell script
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set3 = set1.symmetric_difference(set2)
print(set3)
```

</details>
Ta có thể sử dụng toán tử '^' thay cho symmetric_difference() và sẽ nhận được kết quả tương tự
<details>
  
```shell script
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set3 = set1 ^ set2
print(set3)
```

</details>
Phương pháp symmetric_difference_update() cũng sẽ giữ lại tất cả các phần tử ngoại trừ phần tử trùng lặp, nhưng nó sẽ thay đổi tập hợp gốc thay vì trả về một tập hợp mới.
<details>
  
```shell script
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set1.symmetric_difference_update(set2)
print(set1)
```

</details>


## 3. Python Dictionaries
### Dictionary
Từ điển được sử dụng để lưu trữ giá trị dữ liệu theo cặp khóa:giá trị

Từ điển được viết bằng dấu ngoặc nhọn và có các khóa và giá trị
<details>
  
```shell script
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
```

</details>

#### - Dictionary Items
Các mục trong từ điển được sắp xếp theo thứ tự, có thể thay đổi và không được trùng lặp

Các mục từ điển được trình bày theo cặp khóa:giá trị và có thể được tham chiếu bằng cách sử dụng tên khóa

Từ điển có thể thay đổi, nghĩa là chúng ta có thể thay đổi, thêm hoặc xóa các mục sau khi từ điển đã được tạo.
<details>
  
```shell script
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict["brand"])
```

</details>
Từ điển không thể có hai mục có cùng khóa

Các giá trị trùng lặp sẽ ghi đè lên các giá trị hiện có
<details>
  
```shell script
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964,
  "year": 2020
}
print(thisdict)
```

</details>
#### - Dictionary Items - Data Types
Các giá trị trong các mục từ điển có thể thuộc bất kỳ kiểu dữ liệu nào
Theo quan điểm của Python, từ điển được định nghĩa là các đối tượng có kiểu dữ liệu 'dict'

#### - The dict() Constructor
Có thể sử dụng hàm tạo dict() để tạo một từ điển.
<details>
  
```shell script
thisdict = dict(name = "John", age = 36, country = "Norway")
print(thisdict)
```

</details>
### Access Dictionary Items
#### - Accessing Items
Có thể truy cập các mục trong từ điển bằng cách tham chiếu đến tên khóa của nó, bên trong dấu ngoặc vuông

Ví dụ lấy giá trị của khóa "model"
<details>
  
```shell script
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict["model"]
```

</details>
Ngoài ra còn có một phương pháp được gọi get()là sẽ cho bạn kết quả tương tự
<details>
  
```shell script
x = thisdict.get("model")
```

</details>
#### - Get Keys
Phương pháp keys() sẽ trả về danh sách tất cả các khóa trong từ điển

Nhận danh sách các keys
<details>
  
```shell script
x = thisdict.keys()
```

</details>
Danh sách khóa là dạng xem của từ điển, nghĩa là mọi thay đổi được thực hiện trong từ điển sẽ được phản ánh trong danh sách khóa
#### - Get Values
Phương pháp values() sẽ trả về danh sách tất cả các giá trị trong từ điển

Nhận danh sách các giá trị
<details>
  
```shell script
x = thisdict.values()
```

</details>
Danh sách các giá trị là dạng xem của từ điển, nghĩa là mọi thay đổi được thực hiện trong từ điển sẽ được phản ánh trong danh sách values

Ví dụ thực hiện thay đổi trong từ điển gốc và xem danh sách giá trị cũng được cập nhật
<details>
  
```shell script
car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}

x = car.values()

print(x) #Trước thay đổi

car["year"] = 2020

print(x) #Sau thay đổi
```

</details>

#### - Get Items
Phương pháp items() sẽ trả về từng mục trong từ điển dưới dạng các bộ trong danh sách

Nhận danh sách các cặp khóa:giá trị
<details>
  
```shell script
x = thisdict.items()
```

</details>

#### - Check if Key Exists
Để xác định xem khóa được chỉ định có trong từ điển hay không, ta sử dụng từ khóa 'in':

Ví dụ kiểm tra xem "model" có trong từ điển không
<details>
  
```shell script
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
if "model" in thisdict:
  print("True!")
```

</details>
### Change Dictionary Items
#### - Change Values
Ta có thể thay đổi giá trị của một mục cụ thể bằng cách tham chiếu đến tên khóa của mục đó

Đổi "năm" thành 2018
<details>
  
```shell script
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["year"] = 2018
```

</details>
#### - Update Dictionary
Phương pháp update() sẽ cập nhật từ điển bằng các mục từ đối số đã cho

Đối số phải là một từ điển hoặc một đối tượng có thể lặp lại với các cặp khóa:giá trị

Ví dụ cập nhật "năm" của xe bằng cách sử dụng phương pháp update()
<details>
  
```shell script
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"year": 2020})
```

</details>
### Add Dictionary Items
#### - Adding Items
Việc thêm một mục vào từ điển được thực hiện bằng cách sử dụng khóa chỉ mục mới và gán giá trị cho khóa đó
<details>
  
```shell script
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["color"] = "red"
print(thisdict)
```

</details>
#### - Update Dictionary
Phương pháp update() sẽ cập nhật từ điển với các mục từ một đối số nhất định. Nếu mục không tồn tại, mục sẽ được thêm vào

Đối số phải là một từ điển hoặc một đối tượng có thể lặp lại với các cặp khóa:giá trị
<details>
  
```shell script
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"color": "red"})
```

</details>


### Remove Dictionary Items
#### - Removing Items
Có một số phương pháp để xóa các mục khỏi từ điển
<details>
  
```shell script
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.pop("model") //Phương pháp pop()xóa mục có tên khóa được chỉ định
print(thisdict)

//hoặc

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.popitem() //Phương pháp popitem() xóa mục được chèn cuối cùng (trong các phiên bản trước 3.7, một mục ngẫu nhiên sẽ được xóa thay thế)
print(thisdict)

//hoặc

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict["model"] //Từ del khóa xóa mục có tên khóa được chỉ định
print(thisdict)

//hoặc

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict //Từ delkhóa cũng có thể xóa hoàn toàn từ điển
print(thisdict)

//hoặc

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.clear() Phương pháp clear()làm trống từ điển
print(thisdict)

```
</details>
### Loop Dictionaries
#### - Loop Through a Dictionary
Ta có thể lặp qua một từ điển bằng cách sử dụng vòng lặp for

Khi lặp qua một từ điển, giá trị trả về là các khóa của từ điển, nhưng cũng có các phương thức để trả về các giá trị 

Ví dụ

<details>
  
```shell script
for x in thisdict:
  print(x) // In tất cả các tên khóa trong từ điển, từng cái một

for x in thisdict.values():
  print(x) // In tất cả các giá trị trong từ điển, từng cái một

for x in thisdict.values():
  print(x) // Trả về giá trị của một từ điển

for x in thisdict.keys():
  print(x) // Trả về khóa của một từ điển

for x, y in thisdict.items():
  print(x, y) // Lặp qua cả khóa và giá trị bằng cách sử dụng phương pháp items()
```

</details>

### Copy Dictionaries
#### - Copy a Dictionary
Không thể sao chép một từ điển chỉ bằng cách nhập dict2 = dict1

Vì: dict2 sẽ chỉ là tham chiếu đến dict1, và những thay đổi được thực hiện trong dict1, cũng sẽ tự động được thực hiện trong dict2.

Có nhiều cách để tạo bản sao, một trong những cách đó là sử dụng phương pháp Dictionary tích hợp sẵn copy().
<details>
  
```shell script
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
mydict = thisdict.copy() // Tạo một bản sao của từ điển bằng phương pháp copy()
print(mydict)

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
mydict = dict(thisdict) // Tạo một bản sao của từ điển bằng hàm dict()
print(mydict)
```

</details>

### Nested Dictionaries
#### - Nested Dictionaries
Một từ điển có thể chứa nhiều từ điển khác, được gọi là từ điển lồng nhau

Ví dụ tạo một từ điển chứa ba từ điển

<details>
  
```shell script
myfamily = {
  "child1" : {
    "name" : "Emil",
    "year" : 2004
  },
  "child2" : {
    "name" : "Tobias",
    "year" : 2007
  },
  "child3" : {
    "name" : "Linus",
    "year" : 2011
  }
}
```

</details>

#### - Access Items in Nested Dictionaries
Để truy cập các mục từ một từ điển lồng nhau, ta sử dụng tên của từ điển, bắt đầu bằng từ điển bên ngoài

In tên của trẻ 2
<details>
  
```shell script
print(myfamily["child2"]["name"])
```

</details>
#### - Loop Through Nested Dictionaries
Ta có thể lặp qua một từ điển bằng cách sử dụng items()

Lặp qua các khóa và giá trị của tất cả các từ điển lồng nhau
<details>
  
```shell script
for x, obj in myfamily.items():
  print(x)

  for y in obj:
    print(y + ':', obj[y])
```

</details>

