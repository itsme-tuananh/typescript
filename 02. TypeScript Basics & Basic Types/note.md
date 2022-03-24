Core Type
number - Tất cả số, không có sự phân biệt giữa số nguyên và số dấu phẩy động
string - Tất cả giá trị text
boolean - true / false. Chỉ nhận 2 giá trị đó, không "truthy" hay "falsy"
object - Bất kì JavaScript Object nào, có thể là Type cụ thể hơn (type of object)
Array - Bất kì JavaScript Array nào, Type có thể linh động hoặc strict (về Type của Element)
Tuple - Được thêm bởi TypeScript: Fixed-length Array
Enum - Được thêm bởi TypeScript: Tự động liệt kê Global Constant Identifier
Any - Bất kì giá trị nào, không gán Type cụ thể

JavaScript sử dụng "dynamic type" (resolved at runtime), TypeScript sử dụng "static type" (set during development)

Type Assigment - Trực tiếp gán Type
Type Inference - TypeScript tự động gán Type dựa trên giá trị ban đầu

Union Type - type_1 | type_2 | ...

Literal Type - Giá trị cụ thể

Type Alias - Định nghĩa Custom Type

Function Return Type - Type của giá trị trả về
Function Return Type nhận void (undefined) khi Function không return
undefined có thể được sử dụng như một Type thông thường
Function Return Type nhận undefined khi return;

Function có thể sử dụng dưới dạng Type

unknown - Có thể nhận bất kì giá trị nào nhưng luôn thuộc Type unknown

never - Function không trả về giá trị (clear hơn void)
