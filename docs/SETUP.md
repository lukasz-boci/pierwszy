# Instalacja i Konfiguracja

## Wymagania

- Node.js 16+ 
- npm lub yarn
- Konto Google (dla Gemini API)
- PSN konto (dla PS5 danych)

## Kroki instalacji

### 1. Klonowanie repozytorium

```bash
git clone https://github.com/lukasz-boci/pierwszy.git
cd pierwszy
```

### 2. Instalacja zależności Backend

```bash
cd backend
npm install
```

### 3. Instalacja zależności Frontend

```bash
cd ../frontend
npm install
```

## Konfiguracja

### Backend (.env)

1. Skopiuj `.env.example` na `.env`:
```bash
cd backend
cp .env.example .env
```

2. Uzupełnij zmienne:
   - `GEMINI_API_KEY`: Uzyskaj klucz z [Google AI Studio](https://aistudio.google.com/app/apikey)
   - `PS5_API_KEY`: Uzyskaj dostęp do PS5 API (wymaga rejestracji u Sony)
   - `PORT`: Port serwera (domyślnie 5000)
   - `FRONTEND_URL`: URL frontendu (domyślnie http://localhost:3000)

### Frontend (.env.local)

1. Skopiuj `.env.local.example` na `.env.local`:
```bash
cd frontend
cp .env.local.example .env.local
```

2. Ustaw `NEXT_PUBLIC_API_URL` na adres backendu (domyślnie http://localhost:5000)

## Uruchomienie aplikacji

### Terminal 1 - Backend

```bash
cd backend
npm run dev
```

Serwer będzie dostępny na `http://localhost:5000`

### Terminal 2 - Frontend

```bash
cd frontend
npm run dev
```

Aplikacja będzie dostępna na `http://localhost:3000`

## Testy

```bash
cd backend
npm test
```

## Produkcja

### Backend

```bash
cd backend
npm run build
npm start
```

### Frontend

```bash
cd frontend
npm run build
npm start
```

## Troubleshooting

### Backend nie odpowiada
- Sprawdź czy proces słucha na porcie 5000
- Sprawdź logi błędów w konsoli

### Gemini API zwraca błędy
- Upewnij się że klucz API jest poprawny
- Sprawdź limit użycia w Google Cloud Console

### Problemy z PS5 API
- Wymaga autoryzacji Sony
- Dokumentacja: [PlayStation Network API](https://playstationnetwork.com/api)
