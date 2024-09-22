# NetPlanConfig là cấu hình mạng được sử dụng trên hệ điều hành Ubuntu để cấu hình địa chỉ IP, gateway, và DNS cho một giao diện mạng cụ thể.

## Cấu trúc cấu hình

```yaml
network:
  ethernets:
    ens33: # tuỳ máy
      dhcp4: false
      addresses: [192.168.45.140/24]
      gateway4: 192.168.45.2
      nameservers:
        addresses: [8.8.8.8, 8.8.4.4]
  version: 2
```

# Giải thích

ethernets: Định nghĩa cấu hình cho các giao diện mạng vật lý.

ens33: Tên của giao diện mạng (thay thế bằng tên giao diện của bạn).

dhcp4: false: Tắt cấu hình DHCP và sử dụng địa chỉ IP tĩnh.

addresses: Địa chỉ IP tĩnh của giao diện mạng (với subnet mask).

gateway4: Địa chỉ gateway để truy cập mạng ngoài.

nameservers: Định nghĩa các máy chủ DNS để phân giải tên miền.

addresses: Các địa chỉ IP của máy chủ DNS (ở đây là của Google: 8.8.8.8 và 8.8.4.4).

version: 2: Phiên bản của cấu hình NetPlan.
