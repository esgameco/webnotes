# Cookie Parser Module

More Info: [https://www.npmjs.com/package/@types/cookie-parser](https://www.npmjs.com/package/@types/cookie-parser)

## Install

```bash
npm install --save @types/cookie-parser
```

## Usage

```typescript
import express from 'express';
import cookieParser from 'cookie-parser';

const app: express.Application = express();

app.use(cookieParser);

app.get((req: express.Request, res: express.Response) => {
    console.log(req.cookies);
    res.cookie('key', 'value');
});
```