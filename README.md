# LAUNCH - AI-Powered Stock Analysis

A modern web application that provides AI-powered stock analysis using OpenAI's GPT-4. Enter any stock ticker symbol to receive comprehensive insights including pros, cons, company description, and an investment attractiveness score.

**Final Project for CS 391: Web Application Development Fall 2025**  
**Boston University**  
**Professor: Taymaz Davoodi**

## LIVE DEMO

Visit **[LAUNCH](https://ipo-tracker-two.vercel.app)** to try the application without any setup!

## Features

- **AI-Powered Analysis**: Leverages GPT-4 to analyze stocks and provide detailed investment insights
- **Comprehensive Reports**: View company descriptions, pros and cons, and quantitative attractiveness scores
- **Modern UI**: Clean, minimalist interface with smooth animations and responsive design
- **MongoDB Integration**: Stores analyzed tickers and scores for future reference
- **Real-time Analysis**: Get instant stock analysis results

## Tech Stack

- **Framework**: [Next.js 16](https://nextjs.org/) (App Router)
- **Language**: TypeScript
- **Styling**: [Tailwind CSS 4](https://tailwindcss.com/)
- **AI**: [OpenAI API](https://openai.com/) (GPT-4)
- **Database**: [MongoDB](https://www.mongodb.com/)
- **Runtime**: React 19

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js 20.9.0 or higher
- npm or yarn
- MongoDB instance (local or Atlas)
- OpenAI API key

## Installation

1. **Clone the repository**
```bash
   git clone https://github.com/shreyj03/ipo-tracker.git
   cd ipo-tracker
```

2. **Install dependencies**
```bash
   npm install
```

3. **Set up environment variables**
   
   Create a `.env.local` file in the root directory:
```env
   MONGODB_URI=your_mongodb_connection_string
   OPENAI_API_KEY=your_openai_api_key
```

4. **Run the development server**
```bash
   npm run dev
```

5. **Open your browser**
   
   Navigate to [http://localhost:3000](http://localhost:3000)

## Project Structure
```
ipo-tracker/
├── app/
│   ├── api/
│   │   └── openai.ts          # OpenAI integration and server actions
│   ├── report/
│   │   └── [ticker]/
│   │       ├── page.tsx       # Stock analysis results page
│   │       └── loading.tsx    # Loading state
│   ├── search/
│   │   └── page.tsx           # Search page for entering tickers
│   ├── globals.css            
│   ├── layout.tsx             
│   └── page.tsx               # Landing page
├── lib/
│   └── insertNewTicker.ts     # MongoDB insert function
├── public/                    
├── db.ts                      # MongoDB connection utilities
├── types.ts                   # TypeScript type definitions              
├── package.json
├── tsconfig.json
└── README.md
```

## Contributing

This project is part of a team collaboration. Current team members:
- **sShrey Jain3** - Search page & integration
- **Ibrahim Hussain** - LLM integration & results
- **Yihang Duanmu** - Database integration
- **David Ren** - Landing page

## Known Issues

- The OpenAI API may not have access to very recent IPO data
- Analysis is based on GPT-4's training data and may not reflect real-time market conditions
- Rate limits apply based on your OpenAI API plan

## License

This project is private and maintained by the development team.

## Acknowledgments

- [Next.js](https://nextjs.org/) - React framework
- [OpenAI](https://openai.com/) - AI-powered analysis
- [MongoDB](https://www.mongodb.com/) - Database
- [Tailwind CSS](https://tailwindcss.com/) - Styling
- [Vercel](https://vercel.com/) - Hosting platform
