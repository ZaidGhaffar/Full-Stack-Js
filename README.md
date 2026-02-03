# Js
## Concepts:
**Aysnc**  By Default

**Prototype Inheritance**: unlike Python Js don't have classes, objects inherit properties from other objects. via prototype not by class blueprint.
```
console.log(name);  // Output: undefined (not an error!)
var name = "John";
console.log(name);  // Output: "John"
```
**Output:**
```
var name;           // Declaration hoisted to top
console.log(name);  // undefined
name = "John";      // Assignment stays in place
console.log(name);  // "John"
```

## Tec Stack:
### Frontend:
- **React With Vite**: Vite is 10-100x faster than older bundlers
- **TypeScript** (essential for professional work, catches bugs before runtime)
- **Axios** (for making HTTP requests to the backend)
- **TanStack Query (React Query)**: Industry standard for API calls, caching, and state management

### BackendL
- **FastAPI**: with Pydantic for validation
- **CORS middleware**: configured properly
- **Python-multipart**: for file uploads (images to your model)


## Importance of This Techstack:
- **TypeScript**: catches 90% of bugs before they reach production
- **TanStack Query**: handles loading states, caching, retries automatically
- **Vite**: is 10-100x faster than older bundlers
- **This is what modern startups/companies use in 2025**


## File Structure:
```
my-ml-app/
├── frontend/                    # React app
│   ├── public/
│   │   └── assets/             # Static images, icons
│   ├── src/
│   │   ├── api/                # API client setup
│   │   │   ├── axios.ts        # Axios instance with base URL
│   │   │   └── endpoints.ts    # All API endpoints
│   │   ├── components/         # Reusable components
│   │   │   ├── common/         # Buttons, inputs, cards
│   │   │   ├── forms/          # Form components
│   │   │   └── layout/         # Header, footer, sidebar
│   │   ├── features/           # Feature-based organization
│   │   │   ├── prediction/     # ML prediction feature
│   │   │   │   ├── components/ # Feature-specific components
│   │   │   │   ├── hooks/      # Custom hooks for this feature
│   │   │   │   └── types.ts    # TypeScript types
│   │   │   └── upload/         # File upload feature
│   │   ├── hooks/              # Global custom hooks
│   │   │   └── useModelPrediction.ts
│   │   ├── types/              # Global TypeScript types
│   │   │   └── api.types.ts
│   │   ├── utils/              # Helper functions
│   │   │   └── formatters.ts
│   │   ├── App.tsx
│   │   ├── main.tsx
│   │   └── vite-env.d.ts
│   ├── .env.development
│   ├── .env.production
│   ├── package.json
│   ├── tsconfig.json
│   └── vite.config.ts
│
└── backend/                     # FastAPI app
    ├── app/
    │   ├── api/
    │   │   ├── endpoints/
    │   │   │   ├── predict.py
    │   │   │   └── upload.py
    │   │   └── deps.py         # Dependencies
    │   ├── core/
    │   │   ├── config.py       # Settings
    │   │   └── security.py     # CORS, auth
    │   ├── models/             # Pydantic models
    │   │   ├── request.py
    │   │   └── response.py
    │   ├── services/           # Business logic
    │   │   └── ml_service.py   # Your ML model here
    │   ├── ml_models/          # Saved model files
    │   │   └── model.pkl
    │   └── main.py
    ├── requirements.txt
    └── .env

```