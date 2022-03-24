- Intersection Type

type No1 = ...
type No2 = ...
type Intersection = No1 & No2

- Với Interface chính là extends
  interface Intersection extends No1, No2

- Đối với Object / Interface => Kết hợp
- Còn lại => Điểm chung

- Type Guard

- if (typeof ... === '...') {...}
- if ('property' in object) {...}
- if (object instanceof Class) {...}

- Discriminated Union: Một Pattern, sử dụng đối với Object / Interface, khi mà mỗi Object / Interface là thành phần của Union Type đều có chung một Property xác định loại của Object / Interface đó nhằm đảm bảo tính chính xác khi sử dụng Property của các Object / Interface tạo nên Union Type

- Type Casting: Chỉ định Type cụ thể cho một số giá trị mà TypeScript không thể phát hiện Type một cách chính xác

const userInputElement = <HTMLInputElement>document.getElementById('user-input')!
const userInputElement = document.getElementById('user-input')! as HTMLInputElement

- !: Biểu thức trước ! không trả về null

- Index Property: Tạo Type / Interface mà không cần biết cụ thể các Property mà nó sẽ chứa
  interface X {
  id: string;
  [prop: string]: string;
  }

- Các Property khác trong Type / Interface cũng phải có cùng Type với Index Property

- Function Overload: Định nghĩa nhiều cách gọi cùng một Function với những tham số khác nhau và thực hiện những tác vụ khác nhau dựa trên các tham số đó (Nạp chồng hàm)
  function add(a: number, b: number): number
  function add(a: string, b: string): string
  function add(a: Combinable, b: Combinable) {...}


- Optional Chaining: Truy cập Nested Object / Nested Property an toàn bằng cách kiểm tra nếu phần phía trước ? nếu là undefined sẽ không truy cập phần phía sau ?. Tương tự với if (object && object.property) {...}
  object?.property


- Nullish Coalescing: Chỉ khi giá trị trước ?? là null hoặc undefined mới sử dụng Fallback Value
  const x = y ?? 'default value'