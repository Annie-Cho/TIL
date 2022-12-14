## ๐ Nestjs

- ํจ์จ์ ์ด๊ณ  ํ์ฅ ๊ฐ๋ฅํ Node.js ์๋ฒ ์ธก ์ ํ๋ฆฌ์ผ์ด์์ ๊ตฌ์ถํ๊ธฐ ์ํ ํ๋ ์์ํฌ

### Nestjs์ ํน์ง

- ํ์ฅ์ด ๊ฐ๋ฅํ๊ณ  ์ ์ง ๊ด๋ฆฌ๊ฐ ์ฌ์ด ์๋ฒ ์ ํ๋ฆฌ์ผ์ด์์ ์ฝ๊ฒ ๊ฐ๋ฐํ  ์ ์๋ค.
- TypeScript๋ฅผ ์ ๊ทน์ ์ผ๋ก ๋์ํจ์ผ๋ก์ ์๋ฒ ๊ฐ๋ฐ ์ ๋ฐ์ํ  ์ ์๋ ์ค๋ฅ๋ค์ ์ฌ์ ์ ๋ฐฉ์งํ  ์ ์๋๋ก ํ์๋ค.
- module์ ํตํด ํ์ฅ์ด ์ฉ์ดํ๋๋ก ์ค๊ณ๋์ด์๋ค.
- Nest๋ typescript๋ฅผ ์ฌ์ฉํ๋ฉฐ DI(Dependency Injection), IoC(Inversion of Control), ๋ชจ๋์ ํตํ ๊ตฌ์กฐํ ๋ฑ์ ๊ธฐ์ ์ ํตํด ์์ฐ์ฑ์ด ๋๋ค.
- Nestjs ํ๋ก์ ํธ๊ฐ ์์ฑ๋ ํ ๋๋ ํ ๋ฆฌ ๊ตฌ์กฐ๋ ์๋์ ๊ฐ๋ค.

<p align="center">
<img width="627" alt="แแณแแณแแตแซแแฃแบ 2022-11-23 แแฉแแฎ 11 43 26" src="https://user-images.githubusercontent.com/99185757/203575249-387626c4-9f02-4d44-ba47-21acf70da4c3.png">
</p>
  
- ์ฌ์ค,, ๊ฐ์ธ์ ์ผ๋ก docs ๋ํ ์์ธํ๊ฒ ์ ๋ง๋ค์ด์ ธ์๋ ๊ฒ ๋ง์์ ๋ ๋ค.(์ฌ์ฉ์์ ํธ๋ฆฌ์ฑ?)

<br>

## ๐ Express

- ์น ๋ฐ ๋ชจ๋ฐ์ผ ์ ํ๋ฆฌ์ผ์ด์์ ์ํ ์ผ๋ จ์ ๊ฐ๋ ฅํ ๊ธฐ๋ฅ์ ์ ๊ณตํ๋ ๊ฐ๊ฒฐํ๊ณ  ์ ์ฐํ Node.js ์น ์ ํ๋ฆฌ์ผ์ด์ ํ๋ ์์ํฌ
- Node.js(์๋ฒ์์ JavaScript๊ฐ ์๋๋๋๋ก ํด์ฃผ๋ ๋ฐํ์ ํ๊ฒฝ)์ ์์น๊ณผ ๋ฐฉ๋ฒ์ ์ด์ฉํ์ฌ ์น ์ ํ๋ฆฌ์ผ์ด์์ ๋ง๋ค๊ธฐ ์ํ ํ๋ ์์ํฌ์ด๋ค.

### Express ํน์ง

- ๊ฐ์ฅ ๋ง์ด ์ฌ์ฉํ๋ node.js ํ๋ ์์ํฌ๋ก ๋ง์ ๊ฐ๋ฐ์๋ค์๊ฒ ์ฝ๋์ ๊ตฌ์กฐ์ ํต์ผ์ฑ์ ํฅ์์ํฌ ์ ์๋ค.
- Typescript๋ฅผ express์์ ์ฌ์ฉํ  ์ ์์ง๋ง, tsconfig.json, lint.json ๋ฑ๋ฑ์ jsonํ์ผ์ ๋ง๋ค๊ณ  ์ธํํ๋ ๊ณผ์ ์ด ๋ณต์กํ๋ค.

<br>

## ๐ Nestjs์ Express์ ์ฐจ์ด์ 

- Nestjs๋ ์ํคํ์ฒ์ ์ ์๋ ํ๋ ์์ํฌ์์ ์ ๊ณตํ๊ธฐ ๋๋ฌธ์ ๊ฐ ๊ฐ๋ฐ์๋ค์ ์ํคํ์ฒ๊ฐ ํต์ผ๋๊ณ  ์๋ก ์์ฑํ ์ฝ๋์ ๊ตฌ์กฐ๋ฅผ ์ฝ๊ฒ ํ์ํ  ์ ์๋ค.
- ๋ผ์ฐํ์ ์ฐจ์ด : Express๋ ๋ผ์ฐํ์ํ  ๋ app.use์ฒ๋ผ ๋ฑ๋กํด์ ์ฌ์ฉํ๋ค. ํ์ง๋ง Nestjs๋ ๋ชจ๋ ๋ณ๋ก ๋๋์ด์ ๋ผ์ฐํ์ ํ๋ค.
>๐ก ๋ผ์ฐํ : ๋คํธ์ํฌ์์ ๊ฒฝ๋ก๋ฅผ ์ ํํ๋ ํ๋ก์ธ์ค
    
- ์ปจํธ๋กค๋ฌ์ ์ฐจ์ด : Nestjs๋ ํด๋์ค ๋ณ๋ก ์ปจํธ๋กค๋ฌ์์ method์ ๋ฐ์ฝ๋ ์ดํฐ๋ฅผ ์ฌ์ฉํ๋ค. Auth์์๋ ๋ฐ์ฝ๋ ์ดํฐ๋ฅผ ์ฌ์ฉํ๋ค.
    - ๋ฐ์ฝ๋ ์ดํฐ๋ ํด๋์ค, ๋ฉํ๋ฐ์ดํฐ๋ฅผ ์ฐธ๊ณ ํด์ Nest๊ฐ ๋ผ์ฐํ ๋งต์ ๋ง๋ค ์ ์๋๋กํ๋ค. ์ปจํธ๋กค๋ฌ ๋ด์ฉ์ ๋ง๊ฒ๋ ์์ฒญ์ ๋ฌถ์ด์ฃผ๋ ์ฉ๋?

<p align="center">
 <img width="630" alt="แแณแแณแแตแซแแฃแบ 2022-11-23 แแฉแแฎ 11 46 20" src="https://user-images.githubusercontent.com/99185757/203575872-3154c8cf-cb47-44c0-b36c-f1c65008e481.png">
</p>
    
- ์๋น์ค์ ์ฐจ์ด : Nestjs์ ๊ฒฝ์ฐ ํจ์ ์ธ์๋ก ์ธํฐํ์ด์ค๋ก ์ ํ ๊ฐ๋ค์ด ๋ค์ด์จ๋ค.

<p align="center">
<img width="621" alt="แแณแแณแแตแซแแฃแบ 2022-11-23 แแฉแแฎ 11 47 32" src="https://user-images.githubusercontent.com/99185757/203576102-c9cb5b8a-6cde-4b89-920b-ba48b4e151ef.png">
</p>
