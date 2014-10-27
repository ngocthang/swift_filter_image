<h2>About swift</h2>

Swift là một ngôn ngữ lập trình mới của Apple dành riêng cho hệ điều hành Ios và 
OS X, được xây dựng và tổng hợp từ những ưu điểm tốt nhất của C và Objective C, 
đồng thời lược bỏ những điểm hạn chế của C. Swift đã thay thế một số cấu trúc 
cũ và thay vào đó bằng những đặc điểm mới để tạo thành 1 ngôn ngữ dễ học, 
linh động và vô cùng thú vị.

Apple đã xây dựng Swift bằng cách nâng cấp những compiler trước đây, debugger 
và những framwork cơ sở. Apple đã đơn giản quá việc quản lý bộ nhớ bằng bộ 
đếm tham chiếu tự động (ARC).

Swift hội tụ những ưu điểm nổi bật nhất của các ngôn ngữ hiện đại cộng với sự 
cải tiến thú vị của Apple, Compiler đc tối ưu hoá performance.Thật thú vị khi 
bắt tay vào học swift từ "hello world" cho đến khi tạo những hệ thống phức 
tạp vì swift sẽ là tương lai của những ứng dụng Apple.

<h2>A Swift Tour </h2>

Hầu hết với mỗi người lập trình viên khi học 1 ngôn ngữ mới đều bắt đầu yimf cách 
in được dòng chữ "Hello world", với Swift đơn giản chỉ cần:

println("Hello world!")

và trong swift, chỉ cần 1 câu lệnh trên là đủ để chạy 1 chương trình mà không cần 
add thêm thư viện function,không cần khai báo hàm main và đặc biệt, kết thúc mỗi câu
lệnh thì không cần có dấu ";"

<h3>Simple Values</h3>

- Để khai báo hằng số, dùng "let" và dùng "var" để khai báo biến.Khi khai báo bắt buộc
phải có giá trị khởi tạo.Khai báo biến có thể không cần chỉ ra type nhưng khi đã khai 
báo type thì nếu gán giá trị biến và hằng thì chúng phải đúng type và ta đã khai báo.
Dùng dấu ":" sau tên biến + (kiểu dữ liệu) để khai báo type.

VD: let myConstant = 29<br />
    var myVariable = 31<br />
    let explicitDouble: Double = 70<br />

Dùng "(\)" để lồng biến vào string.
VD: let a = 3
    let str = "I have (\a) apples"

- Khai báo mảng: Dùng "[]" <br />
VD: var array = ["abc", "xyz", "ghi"]<br />
    array[1] = "def"<br />

var arrayIndex = [
    "man": "Thang"
    "woman": "maria"
]<br />

Khai báo mảng rỗng: 
        let emptyArray = [String]()<br />
hoặc    let emptyDic = [String: Float]() để chỉ rõ kiểu dữ liệu của index và kiểu của
value
hoặc nếu khai báo mảng không cần quan tâm kiểu dữ liệu thì chỉ cần đơn giản khai báo
array = [] hay array = [:]

<h3> Control Flow </h3>
Dùng if và swift để dùng hàm điều kiện và dùng for-in, for, while, do-while để tạo vòng
lặp.Giữa các điều kiện và vòng lặp là dấu "{}"

VD:
let individualScores = [75, 43, 103, 87, 12]<br />
var teamScore = 0<br />
for score in individualScores {<br />
    if score > 50 {<br />
        teamScore += 3<br />
    } else {<br />
        teamScore += 1<br />
    }<br />
}<br />
teamScore<br />

khi sử dụng if, thì kiểu trả về bắt buộc phải là dạng boolean
Có thể sử dụng if kết hợp với let cùng 1 giá trị tuỳ ý, giá trị tuỳ ý này có
thể được gán giá trị hoặc có thể để nil. dấu "?" được đặt sau kiểu của giá trị để đánh dấu đó là
giá trị tuỳ ý.

VD:

var optionalString: String? = "Hello"<br />
optionalString == nil<br />

var optionalName: String? = "John Appleseed"<br />
var greeting = "Hello!"<br />
if let name = optionalName {<br />
    greeting = "Hello, \(name)"<br />
}<br />

<h3>Function và Closures </h3>

Dùng "func" để khai báo hàm, để gọi hàm thì dùng tên hàm kết hợp với các đối số đi kèm 
phù hợp với khi khai báo hàm, dùng "->" để tách các tham số và kiểu trả về
VD: 
func greet(name: String, day: String) -> String {<br />
    return "Hello \(name), today is \(day)."<br />
}<br />
Kết quả:
greet("Bob", "Tuesday")

- Closures: Những đoạn code trong closures có thể truy cập đến các biến và funcrtion tồn tại
trong phạm vi và closures đc tạo ra, hay thậm chí nếu closures ở ngoài phạm vi khi nó được 
thực thi. Có thể viết 1 closures mà ko cần khai báo tên, code được bao quanh bởi ({}). Dùng 
"in" để phân tách argument và return type với phần code.

VD:
numbers.map({<br />
    (number: Int) -> Int in<br />
    let result = 3 * number<br />
    return result<br />
})<br />

Khi đã sử dụng thành thạo closures thì ta có thể lược bỏ bớt không cần khai báo kiểu của tham
số, kiểu trả về.
VD:
let mappedNumbers = numbers.map({ number in 3 * number })


<h3>Objects and Class </h3>

Khai báo class: class + tên class. Những thuộc tính bên trong class có thể là biến, hằng, function.
VD:
class Shape {<br />
    var numberOfSides = 0<br />
    func simpleDescription() -> String {<br />
        return "A shape with \(numberOfSides) sides."<br />
    }<br />
}<br />

 

swift_filter_image
==================

- ứng dụng nhỏ để thay đổi màu ngẫu nhiên của bức ảnh. ứng dụng đơn giản chỉ sử dụng 1 imageView, bắt
sự kiện khi click button để chạy hàm random màu sắc.
- Chạy file swift_filter_image.xcodeproj và Run để chạy ứng dụng.
- Click "Apply Filter" để thấy sự thay đổi của bức ảnh
