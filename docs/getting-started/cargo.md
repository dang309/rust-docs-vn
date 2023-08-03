---
sidebar_position: 2
sidebar_label: Cargo
---

# Cargo

Cargo là công cụ dùng để build và quản lý các packages. Nếu bạn đến từ thế giới `JavaScript` thì nó tương tự như [`npm`](https://www.npmjs.com)

Cargo đã được cài đặt cùng với Rust ở phần [Cài đặt](/docs/install). Kiểm tra xem đã cài đặt Cargo thành công hay chưa:
```bash
$ cargo --version
```

Nếu thấy số version dạng x.y.z là thành công, ngược lại là có lỗi (command not found, ...).

## Tạo project với Cargo

Chứng ta hãy tạo lại chương trình Hello World nhưng lần này là với Cargo.

```bash
$ cargo new hello_cargo
$ cd hello_cargo
```

Trong thư mục `hello_cargo`, bạn sẽ thấy 1 file Cargo.toml và thư mục `src` với 1 file `main.rs`.

Mở file Cargo.toml

```yaml title="Cargo.toml"
[package]
name = "hello_cargo"
version = "0.1.0"
edition = "2021"

# See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html

[dependencies]
```

`[package]` bắt đầu phần cấu hình của project hiện tại

`[dependencies]` bắt đầu phần liệt kệ các dependencies của project

:::info
Trong Rust, các packages được gọi là `crates` (Cargo dịch ra là toa hàng, crate là kiện hàng nằm trong các toa hàng)
:::

Tiếp tục với file `src/main.rs`

```rust title="src/main.rs"
fn main() {
    println!("Hello, world!");
}
```

Cargo tự động sinh ra chương trình Hello World giống như chúng ta đã viết ở trên.

Tất cả code của chúng ta sau này đều sẽ nằm trong thư mục `src`.

## Build & Run Cargo project

Để build (hay còn gọi là compile) với Cargo chúng ta dùng câu lệnh:
```bash
$ cargo build
   Compiling hello_cargo v0.1.0 (file:///projects/hello_cargo)
    Finished dev [unoptimized + debuginfo] target(s) in 2.85 secs
```

Câu lệnh này sẽ tạo ra 1 executable file `./target/debug/hello_cargo` (hoặc `.\target\debug\hello_cargo.exe` trên Windows). Để chạy chương trình thì chúng ta chỉ cần gọi file này

```bash
$ ./target/debug/hello_cargo # or .\target\debug\hello_cargo.exe on Windows
Hello, world!
```

Chúng ta cũng có thể sử dụng câu lệnh `cargo run` để vừa build vừa run khá là tiện lợi
```bash
$ cargo run
    Finished dev [unoptimized + debuginfo] target(s) in 0.0 secs
     Running `target/debug/hello_cargo`
Hello, world!
```

Ngoài ra, Rust còn cung cấp 1 câu lệnh `cargo check` để kiểm tra xem chương trình của chúng ta có lỗi gì lúc build hay không. Nó tương tự như `cargo build` nhưng nhanh hơn rất nhiều. Đối với các dự án lớn thì việc build tốn khá nhiều thời gian vì vậy người ta thường dùng `cargo check` để kiểm tra lỗi trước khi thật sự build.

## Recap

* Tạo dự án mới với `cargo new`.
* Biên dịch với `cargo build`.
* Biên dịch và chạy với `cargo run`.
* Kiểm tra lỗi chương trình nhưng không tạo ra executable file `cargo check`.