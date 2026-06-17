# thong-design-website
# THONG DESIGN - Kiến Trúc Hệ Thống

## 📋 Tổng Quan Kiến Trúc

Kiến trúc của THONG DESIGN được thiết kế để hỗ trợ 4 dòng dịch vụ chính với hiệu suất cao và trải nghiệm người dùng tối ưu.

```mermaid
graph TB
    subgraph Client["🖥️ Lớp Giao Diện Người Dùng"]
        WEB["Website HTML/CSS/JS<br/>Responsive Design"]
        MOBILE["📱 Mobile Responsive"]
        CONTACT["📞 Floating Contact Widget"]
    end

    subgraph Frontend["🎨 Lớp Hiển Thị"]
        NAV["Navigation Bar<br/>glassmorphism"]
        HEADER["Hero Section<br/>Background Image + CTA"]
        SERVICES["Services Grid<br/>3 Column Layout"]
        GALLERY["Fleet Gallery<br/>Swiper Carousel"]
        FOOTER["Footer<br/>Contact Info"]
    end

    subgraph Services["🛠️ Lớp Dịch Vụ Chính"]
        SERVICE1["Thiết Kế File & Photoshop<br/>Corel Draw + Adobe Suite"]
        SERVICE2["Phục Hồi Ảnh Cũ<br/>AI + Photoshop Technique"]
        SERVICE3["Thẻ PVC GPS Đa Năng<br/>RFID + GPS Integration"]
        SERVICE4["Cho Thuê Xe Du Lịch<br/>Fleet Management 4-45 Seats"]
    end

    subgraph Backend["⚙️ Lớp Xử Lý Backend"]
        FORM["Form Handler<br/>Contact Requests"]
        EMAIL["Email Service<br/>Notification"]
        ZALO["Zalo Integration<br/>WhatsApp API"]
        PHONE["Phone Service<br/>24/7 Hotline"]
    end

    subgraph Database["💾 Lớp Dữ Liệu"]
        CONTACTS["Contact Database<br/>User Inquiries"]
        SERVICES_DB["Services Database<br/>Fleet Info"]
        PORTFOLIO["Portfolio Database<br/>Project Gallery"]
    end

    subgraph External["🌐 Dịch Vụ Bên Ngoài"]
        GOOGLE_MAPS["Google Maps API<br/>Location Display"]
        UNSPLASH["Unsplash Images<br/>Stock Photos"]
        FONTS["Google Fonts<br/>Typography"]
        ICONS["FontAwesome Icons<br/>UI Elements"]
    end

    subgraph Utils["🔧 Tiện Ích & Thư Viện"]
        TAILWIND["Tailwind CSS<br/>Styling Framework"]
        SWIPER["Swiper.js<br/>Carousel Library"]
        AOS["AOS.js<br/>Scroll Animation"]
        RESPONSIVE["Responsive Design<br/>Mobile First"]
    end

    Client --> Frontend
    Frontend --> Services
    Services --> Backend
    Backend --> Database
    Frontend --> External
    Frontend --> Utils
    Backend --> ZALO
    Backend --> PHONE
    Backend --> EMAIL

    style Client fill:#1e293b,stroke:#f59e0b,stroke-width:2px,color:#fff
    style Frontend fill:#334155,stroke:#3b82f6,stroke-width:2px,color:#fff
    style Services fill:#475569,stroke:#ef4444,stroke-width:2px,color:#fff
    style Backend fill:#64748b,stroke:#10b981,stroke-width:2px,color:#fff
    style Database fill:#78909c,stroke:#8b5cf6,stroke-width:2px,color:#fff
    style External fill:#90a4ae,stroke:#06b6d4,stroke-width:2px,color:#fff
    style Utils fill:#a1a9b1,stroke:#ec4899,stroke-width:2px,color:#fff
```

---

## 📊 Kiến Trúc Chi Tiết các Dịch Vụ

### 1. Dịch Vụ Thiết Kế File & Photoshop

```mermaid
graph LR
    CLIENT["👤 Khách Hàng"]
    SUBMIT["📝 Gửi File/Yêu Cầu"]
    TOOLS["🎨 Design Tools<br/>Corel Draw<br/>Photoshop<br/>Adobe Suite"]
    PROCESS["⚙️ Processing<br/>Vector Design<br/>Layer Management<br/>Color Correction"]
    OUTPUT["📤 Xuất File<br/>High-Resolution<br/>CMYK/RGB Profile"]
    DELIVER["📦 Giao Dịch Hoàn Tất"]

    CLIENT --> SUBMIT --> TOOLS --> PROCESS --> OUTPUT --> DELIVER

    style CLIENT fill:#1e293b,stroke:#f59e0b,color:#fff
    style SUBMIT fill:#334155,stroke:#3b82f6,color:#fff
    style TOOLS fill:#475569,stroke:#ef4444,color:#fff
    style PROCESS fill:#64748b,stroke:#10b981,color:#fff
    style OUTPUT fill:#78909c,stroke:#8b5cf6,color:#fff
    style DELIVER fill:#90a4ae,stroke:#06b6d4,color:#fff
```

---

### 2. Dịch Vụ Phục Hồi Ảnh Cũ

```mermaid
graph LR
    INPUT["📸 Ảnh Cũ Hư Hỏng"]
    SCAN["🔍 Quét & Nhận Diện<br/>AI Analysis"]
    REPAIR["🛠️ Xử Lý<br/>Remove Scratches<br/>Color Restoration<br/>Face Reconstruction"]
    ENHANCE["✨ Nâng Cao Chất Lượng<br/>Upscaling<br/>Detail Recovery"]
    OUTPUT["🖼️ Ảnh Số Cao Cấp"]

    INPUT --> SCAN --> REPAIR --> ENHANCE --> OUTPUT

    style INPUT fill:#1e293b,stroke:#f59e0b,color:#fff
    style SCAN fill:#334155,stroke:#3b82f6,color:#fff
    style REPAIR fill:#475569,stroke:#ef4444,color:#fff
    style ENHANCE fill:#64748b,stroke:#10b981,color:#fff
    style OUTPUT fill:#78909c,stroke:#8b5cf6,color:#fff
```

---

### 3. Dịch Vụ Thẻ PVC GPS Đa Năng

```mermaid
graph LR
    DESIGN["🎨 Thiết Kế Thẻ"]
    CHIP["🔌 Tích Hợp Chip<br/>RFID<br/>GPS Module"]
    PRINT["🖨️ In Ấn Trực Tiếp<br/>Full Color<br/>High Resolution"]
    ENCODE["🔐 Mã Hóa Dữ Liệu<br/>Security Encryption<br/>User Database"]
    QA["✅ Kiểm Chất Lượng<br/>Durability Test<br/>Chip Verification"]
    DELIVER["📦 Giao Nhận<br/>Bulk Packaging"]

    DESIGN --> CHIP --> PRINT --> ENCODE --> QA --> DELIVER

    style DESIGN fill:#1e293b,stroke:#f59e0b,color:#fff
    style CHIP fill:#334155,stroke:#3b82f6,color:#fff
    style PRINT fill:#475569,stroke:#ef4444,color:#fff
    style ENCODE fill:#64748b,stroke:#10b981,color:#fff
    style QA fill:#78909c,stroke:#8b5cf6,color:#fff
    style DELIVER fill:#90a4ae,stroke:#06b6d4,color:#fff
```

---

### 4. Dịch Vụ Cho Thuê Xe Du Lịch

```mermaid
graph LR
    BOOKING["📞 Đặt Lịch<br/>Phone/Zalo/Form"]
    SELECT["🚌 Lựa Chọn Xe<br/>4-7 Chỗ<br/>16-29 Chỗ<br/>45 Chỗ Kia Grandbird"]
    CONFIRM["✅ Xác Nhận<br/>Giá & Ngày"]
    INSPECT["🔍 Kiểm Tra Xe<br/>Maintenance<br/>Cleanliness"]
    OPERATE["🚗 Vận Hành<br/>Professional Driver<br/>GPS Tracking"]
    RETURN["🏁 Hoàn Xe<br/>Inspection<br/>Payment"]

    BOOKING --> SELECT --> CONFIRM --> INSPECT --> OPERATE --> RETURN

    style BOOKING fill:#1e293b,stroke:#f59e0b,color:#fff
    style SELECT fill:#334155,stroke:#3b82f6,color:#fff
    style CONFIRM fill:#475569,stroke:#ef4444,color:#fff
    style INSPECT fill:#64748b,stroke:#10b981,color:#fff
    style OPERATE fill:#78909c,stroke:#8b5cf6,color:#fff
    style RETURN fill:#90a4ae,stroke:#06b6d4,color:#fff
```

---

## 🔌 Tích Hợp Hệ Thống Liên Lạc

```mermaid
graph TB
    CUSTOMER["👥 Khách Hàng"]
    
    subgraph CHANNELS["📡 Kênh Liên Lạc"]
        PHONE["☎️ Hotline<br/>090.798.1212"]
        ZALO["💬 Zalo<br/>0933.576.557"]
        EMAIL["📧 Email<br/>thongkythuat@live.com"]
        FORM["📋 Contact Form<br/>Website"]
    end

    subgraph RESPONSE["🔄 Xử Lý Phản Hồi"]
        RECEIVE["Nhận Thông Tin"]
        STORE["Lưu Database"]
        NOTIFY["Gửi Thông Báo"]
        ASSIGN["Phân Công Nhân Viên"]
    end

    subgraph SUPPORT["🛠️ Hỗ Trợ 24/7"]
        TECH["Kỹ Thuật Tư Vấn"]
        SALES["Bán Hàng"]
        LOGISTICS["Vận Hành"]
    end

    CUSTOMER --> CHANNELS
    CHANNELS --> RESPONSE
    RESPONSE --> SUPPORT

    style CUSTOMER fill:#1e293b,stroke:#f59e0b,stroke-width:2px,color:#fff
    style CHANNELS fill:#334155,stroke:#3b82f6,stroke-width:2px,color:#fff
    style RESPONSE fill:#475569,stroke:#ef4444,stroke-width:2px,color:#fff
    style SUPPORT fill:#64748b,stroke:#10b981,stroke-width:2px,color:#fff
```

---

## 🎯 Công nghệ & Stack

| Thành Phần | Công Nghệ |
|-----------|----------|
| **Frontend Framework** | HTML5, CSS3, Tailwind CSS |
| **JavaScript Libraries** | Swiper.js (Carousel), AOS.js (Animations) |
| **Icons & Fonts** | FontAwesome 6.4.0, Google Fonts |
| **Design Tools** | Adobe Photoshop, Corel Draw |
| **AI Technology** | Image Restoration AI |
| **Hardware Integration** | RFID Chips, GPS Modules |
| **APIs** | Google Maps, Zalo, WhatsApp |
| **Responsive Design** | Mobile First, Breakpoints (md, lg) |
| **Performance** | Image Optimization, Lazy Loading |
| **SEO** | Meta Tags, Schema Markup |

---

## 📱 Responsive Design Breakpoints

```
Mobile:     < 640px  (Default)
Tablet:     640px - 1024px (md breakpoint)
Desktop:    > 1024px (lg breakpoint)
```

---

## 🎨 Color Scheme & Branding

```
Primary Dark:     #0b0f19 (brand-dark)
Secondary Dark:   #1e293b (brand-slate)
Accent Gold:      #f59e0b (brand-gold)
Gold Hover:       #d97706 (brand-goldHover)
Accent Blue:      #3b82f6 (brand-accent)
Red CTA:          #ef4444
Blue Secondary:   #0068ff
```

---

## 🚀 Deployment & Hosting

```mermaid
graph LR
    GITHUB["GitHub Repository<br/>Vu-Thong/thong-design-website"]
    BUILD["Build Process<br/>Static Files"]
    HOSTING["Web Hosting<br/>CDN Distribution"]
    USERS["👥 Users Worldwide"]

    GITHUB --> BUILD --> HOSTING --> USERS

    style GITHUB fill:#1e293b,stroke:#f59e0b,color:#fff
    style BUILD fill:#334155,stroke:#3b82f6,color:#fff
    style HOSTING fill:#475569,stroke:#ef4444,color:#fff
    style USERS fill:#64748b,stroke:#10b981,color:#fff
```

---

## 📞 Contact & Support

- **Hotline 24/7:** 090.798.1212
- **Zalo/WhatsApp:** 0933.576.557
- **Email:** thongkythuat@live.com
- **Service Area:** TP. Hồ Chí Minh

---

*Tài liệu này được cập nhật lần cuối: 2026*
