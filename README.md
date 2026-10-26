# 🔒 Numara Hapishanesi

### *Premium 2D Psychological Bluff & Prediction Game*

> Dribbble-trending quality UI • Prison theme • Glassmorphism • Mobile-first

![Game Theme](https://img.shields.io/badge/Theme-Prison-orange) ![UI Quality](https://img.shields.io/badge/UI-Premium-00ff88) ![Mobile](https://img.shields.io/badge/Mobile-First-blue)

---

## 🎮 Konsept

Hapishane temalı, masa başı, psikolojik blöf oyunu. Her mahkuma gizli bir numara verilir. Özel mesajlaşarak blöf yap, ipucu ver veya yanılt. Round sonunda herkesin numarasını tahmin et!

### Premium UI Özellikleri
- 🖤 Derin kömür siyahı arka plan
- 🟠 Hapishane turuncusu accent renkleri
- 🟢 Neon yeşil online durum göstergeleri
- 🔲 Glassmorphism paneller
- ✨ 3D metal doku efektleri
- 📋 Clipboard/mugshot frame tasarımı
- 🔠 Stencil font başlıklar + Typewriter body
- 💡 Neon glow efektleri
- 🎬 Smooth animasyonlar

---

## 🚀 Kurulum

```bash
npm install
npm run dev      # Development
npm run build    # Production build
```

## 🎯 Oyun Akışı

1. **Kayıt** → Kod adı gir, karakterini özelleştir
2. **Lobi** → Bot ekle veya oyuncu bekle (min 2 kişi)
3. **Round Başlar** → Gizli numaralar dağıtılır (120 saniye)
4. **Mesajlaş** → Özel mesajlarla blöf yap (3 hak/round)
5. **Tahmin Et** → Diğer mahkumların numaralarını tahmin et
6. **Sonuçlar** → Numaralar açılır, puanlar güncellenir
7. **Yeni Round** → Tekrar!

## 📁 Mimari

```
src/
├── App.tsx                     # Ana routing
├── types.ts                    # TypeScript tipleri
├── store/
│   └── gameStore.ts           # Zustand state
├── services/
│   ├── gameEngine.ts          # Oyun motoru (simulated server)
│   └── socketEvents.ts        # Socket event dokümantasyonu
├── validators/
│   └── schemas.ts             # Zod validation schemas
├── db/
│   └── schema.ts              # Prisma schema docs
└── components/
    ├── CharacterCreator.tsx    # Premium karakter oluşturma
    ├── CharacterAvatar.tsx     # 2D SVG karakter (premium)
    ├── Lobby.tsx               # Hapishane bekleme odası
    ├── PrisonRoom.tsx          # Ana oyun ekranı
    ├── PrivateChatModal.tsx    # Şifreli iletişim
    ├── GuessPanel.tsx          # Tahmin paneli
    └── RevealScreen.tsx        # Round sonuçları
```

## 🎨 Tasarım Sistemi

### Renk Paleti
| Renk | Hex | Kullanım |
|------|-----|----------|
| Kömür Siyah | `#0a0a0f` | Ana arka plan |
| Çelik Gri | `#2a2a3e` | Paneller |
| Hapishane Turuncu | `#e8720c` | Primary accent |
| Neon Yeşil | `#00ff88` | Online/success |
| Kan Kırmızısı | `#dc2626` | Timer/danger |

### Fontlar
- **Black Ops One** — Stencil başlıklar
- **Special Elite** — Typewriter body text
- **Share Tech Mono** — Monospace data

### Efektler
- Glassmorphism (`backdrop-filter: blur`)
- Metal texture (gradient + inset shadows)
- Neon glow (box-shadow + text-shadow)
- Iron bars overlay (repeating-linear-gradient)
- Spotlight (radial-gradient)
- Scan line animation

## 🔐 Güvenlik

Engine seviyesinde koruma:
- ✅ Mesaj limiti sunucu tarafında kontrol
- ✅ Tahmin validasyonu (1-10, integer)
- ✅ Rate limiting
- ✅ Aynı isim engelleme
- ✅ Disconnect handling

### Production için Eklenmesi Gerekenler
- Socket.io backend
- JWT authentication
- SQLite + Prisma database
- Server-side game authority
- CORS configuration

## 🎮 Mod Sistemi (Placeholder)

| Mod | Açıklama | Durum |
|-----|----------|-------|
| Klasik | 1-10 numara | ✅ Aktif |
| Çift Numara | 2 numara/oyuncu | 🔜 Yakında |
| Yasak Numara | Bazı numaralar kapalı | 🔜 Yakında |
| Bahis | Chip sistemi | 🔜 Yakında |
| Görev | Özel hedefler | 🔜 Yakında |
| Takım | 2v2 / 3v3 | 🔜 Yakında |

## 🐛 Debug

Oyun sırasında sol üst ⚙️ butonu ile:
- Timer'ı kısalt
- Hemen reveal yap
- Yeni round başlat

## 📱 Responsive

- Mobile-first tasarım
- Touch-friendly targets (min 44px)
- Dikey layout
- Safe area desteği

---

*Numara Hapishanesi — Blöf yap. Tahmin et. Hayatta kal.* 🔒
