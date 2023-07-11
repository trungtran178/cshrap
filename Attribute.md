Tổng quan
Thuộc tính (attribute) trong C#, là một thẻ khai báo, được sử dụng để truyền thông tin tới runtime về các hành vi của các phần tử khác nhau như các lớp, phương thức, cấu trúc, enum, assembly… trong chương trình của bạn. 
Bạn có thể thêm thông tin khai báo vào chương trình bằng cách sử dụng attribute.
Một thẻ khai báo được mô tả bởi các dấu ngoặc vuông ([]) đặt bên trên phần tử mà nó được sử dụng cho.
Các Attribute được sử dụng để thêm metadata, ví dụ như chỉ lệnh biên dịch và thông tin khác như comment, mô tả, phương thức và các lớp vào một chương trình. .Net Framework cung cấp hai kiểu attribute: thuộc tính được định nghĩa trước (pre-defined attribute) và thuộc tính tùy chỉnh (custom built attribute).

Định nghĩa một Attribute trong C#
Cú pháp để xác định một Attribute trong C# như sau:
[attribute(positional_parameter, name_parameter = giá_trị, ...)]
element

Tên của Attribute và giá trị của nó được xác định bên trong dấu ngoặc vuông, ở trước phần tử từ đó thuộc tính được áp dụng cho. positional_parameter xác định thông tin thiết yếu và name_parameter xác định thông tin tùy ý.

Attribute được định nghĩa trước trong C#
.Net Framework cung cấp 3 Attribute được định nghĩa trước:

AttributeUsage
Conditional
Obsolete
AttributeUsage trong C#
Attribute được định nghĩa trước AttributeUsage miêu tả cách một lớp custom Attribute có thể được sử dụng. Nó xác định kiểu của các item, mà từ đó Attribute có thể áp dụng cho.

Cú pháp để xác định Attribute này trong C# như sau:
[AttributeUsage(
   validon,
   AllowMultiple=allowmultiple,
   Inherited=inherited
)]

Trong đó:
Tham số validon xác định các phần tử ngôn ngữ mà Attribute có thể được đặt. Nó là một sự tổ hợp giá trị của một AttributeTargets enumerator. Giá trị mặc định là AttributeTargets.All.
Tham số allowmultiple (tùy ý) cung cấp giá trị cho thuộc tính AllowMultiple của attribute này, một giá trị Boolean. Nếu điều này là true, Attribute là multiuse. Giá trị mặc định là false (tức là single-use).
Tham số inherited (tùy ý) cung cấp giá trị cho thuộc tính Inherited của attribute này, một giá trị Boolean. Nếu nó là true, Attribute được kế thừa bởi các lớp kế thừa. Giá trị mặc định là false (không được kế thừa).
