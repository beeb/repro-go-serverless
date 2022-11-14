To reproduce:

- Move into goapp: `cd apps/goapp`
- Setup with `pnpm run setup` or `vercel login && vercel link`
- Try to run `pnpm run start` which calls `vercel dev`
- Observe the error: `Error: repro-go-serverless/apps/goapp/apps/goapp doesn't exist`
- Try to change the run command to: `cd ../.. && vercel dev`
- Try to run `pnpm run start` which calls `vercel dev`
- Server starts on port 3000
- Try to visit [http://localhost:3000/api/hello](http://localhost:3000/api/hello)
- Obersve the error: `502: BAD_GATEWAY Code: NO_RESPONSE_FROM_FUNCTION` in the browser and `2022/11/14 08:00:20 open api/hello.go: no such file or directory` in the console
