# Movie Platform Backend

Ushbu loyiha NestJS, TypeScript va Prisma yordamida yaratilgan kinolar saytining backend qismidir. Unda foydalanuvchilar ro‘yxatdan o‘tishi, tizimga kirishi, kinolarni ko‘rishi, sevimlilarga qo‘shishi, sharh qoldirishi va obuna sotib olishi mumkin.

## Asosiy imkoniyatlar

- Foydalanuvchi autentifikatsiyasi
- Admin va foydalanuvchi rollari
- Kino, kategoriya va sharhlarni boshqarish
- Sevimlilar ro‘yxati
- Premium kontent uchun obuna tizimi
- Poster va video fayllarni yuklash
- Swagger orqali API hujjatlari
- Boshlang‘ich ma’lumotlar uchun seeder

## Texnologiyalar

- NestJS
- TypeScript
- Prisma ORM
- PostgreSQL
- JWT
- Argon2
- Swagger
- Multer

## Tez ishga tushirish

### 1. Bog‘liqliklarni o‘rnatish

```bash
pnpm install
```

### 2. Environment sozlamalari

Loyiha ildizida `.env` faylini yarating:

```env
DATABASE_URL=postgresql://user:password@localhost:5432/kinosayt
JWT_SECRET=your_super_secret_key
PORT=3000
SUPERADMIN_EMAIL=admin@example.com
SUPERADMIN_PASSWORD=StrongPassword123!
```

### 3. Prisma client yaratish

```bash
pnpm prisma generate
```

### 4. Ma’lumotlar bazasini ishga tushirish

```bash
pnpm prisma migrate dev --name init
```

### 5. Ilovani ishga tushirish

```bash
pnpm run start:dev
```

## Muhim manzillar

- API: http://localhost:3000/api/v1
- Swagger: http://localhost:3000/swagger
- Upload fayllar: http://localhost:3000/uploads/...

## Loyiha tuzilishi

```text
prisma/        -> Prisma schema va migratsiyalar
src/           -> Asosiy kodlar
  modules/     -> Auth, profile, movies, subscriptions, favorites, reviews, admin
  common/      -> Guards, decorators, seeder va utilitlar
  core/        -> Prisma va JWT modullari
```

## Eslatma

Agar Prisma generatsiya vaqtida muammo bo‘lsa, quyidagi buyruqni yana ishga tushiring:

```bash
pnpm prisma generate
```
