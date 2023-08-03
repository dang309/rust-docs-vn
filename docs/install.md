---
sidebar_position: 2
sidebar_label: Cài đặt
---

# Cài đặt

Đầu tiên, chúng ta sẽ cài đặt [`rustup`](https://rustup.rs) - trình quản lý version của Rust. Nó tương tự như [`nvm`](https://github.com/nvm-sh/nvm) của NodeJS.

## Cài đặt `rustup` trên Linux và macOS 

```bash
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

Nếu cài đặt thành công, màn hình sẽ xuất hiện dòng chữ sau:

```
Rust is installed now. Great!
```

:::note
Bởi vì 1 số packages của Rust được viết bằng ngôn ngữ C nên chúng ta cần cài đặt trình biên dịch cho C.

MacOS
```bash
xcode-select --install
```

Linux
```bash
sudo apt install build-essential
```
:::

## Cài đặt `rustup` trên Windows

Truy cập [https://www.rust-lang.org/tools/install](https://www.rust-lang.org/tools/install) và làm theo hướng dẫn.