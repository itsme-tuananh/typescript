method(this: Class) {...}

- Truyền tham số this vào method nhằm chỉ định this sẽ tham chiếu tới một Instance của Class (Object với type Class) khi method được thực thi

- private: Đánh dấu Private Property / Method
- public: (Mặc định) Đánh dấu Public Property / Method
- Vanilla JavaScript (đa phần) không biết đến private và public, tất cả Property / Method đều là public

- Shorthand Initialization
  constructor(private p1: string, public p2: number) {...}

- readonly: Đánh dấu Property / Method chỉ đọc, không được thay đổi
- Vanilla JavaScript không biết đến readonly
  private readonly p1: string;

- Một Sub-Class chỉ có thể kế thừa một Base-Class
- Khi Sub-Class sử dụng Contructor riêng, cần sử dụng super() để gọi Constructor của Base-Class
- Luôn gọi super() đầu tiên bên trong Constructor trước khi làm bất cứ điều gì với this

- Sub-Class có thể ghi đè Method của Base-Class
- protected: Đánh dấu Property / Method chỉ được chỉ sử dụng trong một Class và các Class kế thừa Class đó

- getter: Method được sử dụng như Property để get giá trị của Property
  get p1() {
  if (p1) {
  return this.p1;
  }
  throw new Error('...');
  }
- setter: Method được sử dụng như Property để set giá trị của Property
  set p1(value) {
  if (!value) {
  throw new Error('...');
  }
  this.p1 = value;
  }
- getter và setter thường được sử dụng để đóng gói logic và bổ sung thêm logic khi get hoặc set giá trị của Property

- static Property / Method: Được truy cập trực tiếp trên Class mà không cần định nghĩa Instance từ Class đó và không thể sử dụng trên Instance từ Class
- Không thể sử dụng static Property / Method trong non-static Property / Method. Nếu sử dụng static Property / Method bên trong Class, dùng cú pháp ClassName.staticMethodName / ClassName.staticPropertyName

- abstract Property / Method: Không được định nghĩa mà chỉ được khai báo nhằm đảm bảo tất cả Sub-Class kế thừa từ abstract Class phải có và định nghĩa cụ thể cho các abstract Property / Method đó. Class chứa abstract Property / Method trở thành abstract Class và bắt buộc phải thêm từ khóa abstract (abstract class ClassName)
  abstract private p1: string;
  abstract method(): void;
- abstract Class không thể khởi tạo Instance mà chỉ có thể được kế thừa từ các Sub-Class

- Singleton: Một Class chỉ có một Instance
- Private Constructor: Không thể tạo Instance từ Class bên ngoài Class. Triển khai cụ thể bằng static Property và Method cụ thể trong ví dụ...

- Interface: Định nghĩa cấu trúc của Object
- Interface có thể được sử dụng như Type cho Object

- Class có thể sử dụng Interface bằng từ khóa implements
- Một Class có thể implement nhiều InterFace
- Interface đảm bảo các Class implement nó có chung một (số) Property / Method nhất định
- Có thể sử dụng Interface như Type cho các biến, hằng được khởi tạo từ Class implement Interface đó

- Có thể thêm readonly cho các Property / Method trong Interface

- Sử dụng từ khóa extends để kế thừa Interface. Một Interface có thể kế thừa nhiều hơn một Interface khác

- Có thể sử dụng Interface như Function Type (Khai báo giống Method nhưng không có tên (Anonymous Function / Method))
  interface Fn {
  (a: string): number;
  }

- Đánh dấu Optional Property / Method trong Interface, Class với kí tự ?
  optionalProperty?: string
  optionalMethod?() {...}
- Đánh dấu Optional Parameter với kí tự ? (tương đương việc sử dụng Default Value là undefined) hoặc sử dụng Default Value
  Fn(p?: number) {...}

- Interface không được compile sang .js Code. Vanilla JavaScript không biết đến Interface
