# Agentic Coding AI

This project is an interactive coding agent that generates production-ready React web applications using the OpenRouter API and LangChain.

## Features
- Generates complete React 18+ projects (TypeScript, Tailwind CSS)
- Uses modern React patterns (hooks, functional components)
- Beautiful, responsive, mobile-first UI
- CLI interface for user prompts
- Automatically creates project files from LLM output

## Usage
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Run the agent:
   ```bash
   python app.py
   ```

3. Follow the CLI prompts to describe the app you want.

## Example

**Sample Input:**

```
Describe the app you want: create a simple calculator
```

**Sample Output:**

The following files will be generated in the `generated_project/` folder:

- `metadata.json` — Project metadata
- `index.html` — Main HTML file
- `index.tsx` — React entry point
- `App.tsx` — Main app component
- `components/Calculator.tsx` — Calculator UI and logic

**Example: `generated_project/metadata.json`**

```
{
   "name": "Simple Calculator",
   "description": "A responsive calculator application built with React and TypeScript."
}
```

**Example: `generated_project/App.tsx`**

```tsx
import React from 'react';
import Calculator from './components/Calculator';

const App: React.FC = () => {
   return (
      <div className="flex flex-col items-center justify-center h-full">
         <h1 className="text-2xl font-bold mb-4">Simple Calculator</h1>
         <Calculator />
      </div>
   );
};

export default App;
```

## Project Structure
- `app.py` — Main agent code
- `requirements.txt` — Python dependencies
- Generated projects are saved in the `generated_project/` folder

## Environment Variables
- `OPENROUTER_API_KEY` — Set in a `.env` file in the project root. The app uses `python-dotenv` to load this key automatically.


## Additional Notes
- All generated React code uses TypeScript and Tailwind CSS only.
- The agent expects clear, concise app descriptions for best results.
- The project now requires `python-dotenv` (see requirements.txt).

### Example .env file

```
OPENROUTER_API_KEY=your_openrouter_api_key_here
```

---

**Author:** Agentic Coding AI
