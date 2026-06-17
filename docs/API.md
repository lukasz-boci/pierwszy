# API Documentation

## Backend Endpoints

### Health Check

```
GET /api/health
```

Response:
```json
{
  "status": "Backend is running!"
}
```

### Chat with Gemini

```
POST /api/chat
Content-Type: application/json

{
  "message": "How do I beat mission X in GTA V?"
}
```

Response:
```json
{
  "response": "Here's the walkthrough...",
  "message": "How do I beat mission X in GTA V?"
}
```

### Get PS5 Stats

```
GET /api/ps5/stats?psn=YOUR_PSN_HERE
```

Response:
```json
{
  "psn": "your_psn",
  "gta_level": 120,
  "money": 5000000,
  "missions_completed": 85,
  "playtime": "150 hours",
  "achievements": {
    "total": 60,
    "unlocked": 45
  }
}
```

## Gemini Service API

### Chat

```javascript
const response = await geminiService.chat(userMessage, context);
```

### Generate Mission Guide

```javascript
const guide = await geminiService.generateMissionGuide("mission_name");
```

### Analyze Build

```javascript
const analysis = await geminiService.analyzeBuildOptimization(buildInfo);
```

## PS5 Service API

### Get Player Profile

```javascript
const profile = await ps5Service.getPlayerProfile(psn);
```

### Get GTA Stats

```javascript
const stats = await ps5Service.getGTAStats(psn);
```

### Get Achievements

```javascript
const achievements = await ps5Service.getOnlineAchievements(psn);
```
