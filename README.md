# Steady
> Server Side Generated, MDX written articles created with NextJS 14

![Google Lighthouse Report](https://github.com/WillKirkmanM/steady/assets/98240335/33bdd03e-2a9b-45af-92ae-083e53ae1ac3)

## Getting Started
Install Dependencies:
```bash
bun install
```

Run in Development mode:
```bash
bun dev
```

Build for Production:
```bash
bun build
```

Start Production Build:
```bash
bun start
```

## Writing Articles
Articles are written in the `content/articles` folder. The name of the file before the `.mdx` will be the url. 

In MDX you can set the title and description of the article enclosed by the `---` at the top of the file:

```mdx
---
title: "Hello, World!"
description: "What a day to be alive"
---
```

## Custom Components
If you would like to use Custom Components in your articles, you need to include them in the `components/MDX/TheMDXRemote.tsx`:

```
import { Button } from "@/components/ui/button"

const components = {
  Button
}

```

You can also modify existing behaviour:
```ts
  const components = {
    h1: (props) => <h1 className="text-3xl" {...props} />,
    ol: (props: any) => <ol className="list-decimal" {...props} />
  }
```

then in your article:
```mdx
Psychologically, the button has to be one of the most appealing elements on the page. Get that wrong and you fail. Take this button for example:

<Button>Login</Button>

Entranced by the look, you find the feel... and click it. Simply perfect
```
