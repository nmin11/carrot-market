```js
import { NextApiHandler, NextApiRequest, NextApiResponse } from "next";

export const withHandler = (
  method: "GET" | "POST",
  handler: NextApiHandler
): NextApiHandler => {
  return async (req, res) => {
    if (req.method !== method) {
      res.status(405).end();
    }

    try {
      await handler(req, res);
    } catch (error) {
      console.error(error);
      if (error instanceof Error) {
        res.status(500).json({ error: error.message });
      } else {
        res.status(500).json({ error: "Internal Server Error" });
      }
    }
  };
};
```

- 8.4 withHandler에서 수강생이 수정해준 부분
- Reference : [수강생님의 커밋 링크](https://github.com/jinyongp/carrot-market/commit/14bebab033683e45b49db207fd8ce90ae6ee0092)
