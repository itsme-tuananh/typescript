- Generic Type: Thường được kết nối với một Type khác và linh hoạt về Type chính xác mà nó trở thành, bổ sung thông tin về Type đối với những Class, Function phức tạp tác động đến dữ liệu đầu vào, theo một cách không quan tâm tới dữ liệu thuộc một Type cụ thể mà lưu thông tin về Type của dữ liệu đầu vào đó
  function x<T, U>(objA: T, objB: U) {...}

- Constraint: Xác định Type cụ thể mà Generic Type làm cơ sở
  function x<T extends object, U>(objA: T, objB: U) {...}

- The "keyof" Constraint: Đảm bảo Type U là một Property của Type T
  function x<T extends object, U extends keyof T>(objA: T, objB: U) {...}

- Generic Utility Types
  Partial<T>
  Readonly<T>
