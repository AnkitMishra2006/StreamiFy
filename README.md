# StreamiFy

A real-time video streaming and chat application built with React and Node.js.

## Project Structure

```
StreamiFy/
├── frontend/          # React frontend application
├── backend/           # Node.js Express backend
├── package.json       # Root package.json for monorepo
└── vercel.json        # Vercel deployment configuration
```

## Local Development

1. Install dependencies:

```bash
npm install
```

2. Start development servers:

```bash
# Start both frontend and backend
npm run dev

# Or start individually
npm run dev --prefix frontend
npm run dev --prefix backend
```

## Build and Deploy

### Build locally:

```bash
npm run build
```

### Deploy to Vercel:

1. Connect your GitHub repository to Vercel
2. Set the root directory to the project root
3. Vercel will automatically use the `vercel.json` configuration

The build process will:

- Install dependencies for both frontend and backend
- Build the React frontend
- Output static files to `frontend/dist/`

## Environment Variables

Make sure to set up your environment variables in Vercel dashboard:

- Copy variables from `backend/.env.sample`
- Copy variables from `frontend/.env.sample`

## Technologies Used

- **Frontend**: React 18, Vite, TailwindCSS, DaisyUI
- **Backend**: Node.js, Express, MongoDB
- **Real-time**: Stream Chat, Stream Video
- **Deployment**: Vercel
