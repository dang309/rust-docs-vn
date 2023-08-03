---
sidebar_position: 1
sidebar_label: Hello World!
---

# Hello World

Let's say Hello to the World!

:::note
Toàn bộ tài liệu sẽ sử dụng command line và hệ điều hành linux (Ở mức cơ bản thôi!) và giữ nguyên các thuật ngữ chuyên nghành bằng tiếng Anh.
:::

## Tạo thư mục

Linux, macOS, PowerShell:

```bash
$ mkdir ~/projects
$ cd ~/projects
$ mkdir hello_world
$ cd hello_world
```

Windows CMD:

```bash
> mkdir "%USERPROFILE%\projects"
> cd /d "%USERPROFILE%\projects"
> mkdir hello_world
> cd hello_world
```

## Code

Tạo 1 file có tên là `main.rs` và nhập vào đoạn code sau:

```rust title="main.rs"
fn main() {
    println!("Hello, World!");
}
```

:::note
1. Trong Rust, những hàm kết thúc bằng dấu `!` (println!, format!, ...) được gọi là `macros`, nó gần giống với `decorators` trong `Python` hay `Higher Order Function` trong 1 số ngôn ngữ khác.
2. Biểu thức trong Rust bắt buộc kết thúc bằng dấu `;`
3. Chuỗi bắt buộc nằm trong dấu nháy kép `"`
:::

Lưu file và quay trở lại Terminal với đường dẫn `~/projects/hello_world`. Biên dịch và chạy:

```bash
$ rustc main.rs
$ ./main
Hello, world!
```

Nếu màn hình hiện ra `Hello, World!` thì xin chúc mừng. Bạn đã thành công!