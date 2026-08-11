---
layout: post
title: "Bắt đầu hành trình học Malware Analysis"
date: 2026-08-11 10:00:00 +0700
categories: [notes]
tags: [khoi-dau, lo-trinh]
---

Đây là bài viết đầu tiên — mở đầu hành trình học malware analysis của mình.

## Mục tiêu

1. Nắm vững kiến trúc PE file
2. Thành thạo static & dynamic analysis
3. Viết write-up cho từng mẫu malware phân tích được

> ⚠️ Lưu ý: mọi mẫu phân tích đều chạy trong VM cô lập, không kết nối mạng thật.

## Ví dụ hiển thị code

```python
import hashlib

def get_sha256(filepath):
    with open(filepath, "rb") as f:
        return hashlib.sha256(f.read()).hexdigest()

print(get_sha256("sample.bin"))
```

## Bảng IOC mẫu

| Loại | Giá trị |
|------|---------|
| SHA256 | `a1b2c3...` (ví dụ minh họa) |
| C2 Domain | `example[.]bad` |
| File type | PE32 |

<span class="tag-badge">reverse-engineering</span>
<span class="tag-badge">lo-trinh</span>
