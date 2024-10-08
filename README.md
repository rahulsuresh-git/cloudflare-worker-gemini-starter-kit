![Logo](/static/cover.png)

# Cloudflare Worker + Google Gemini Starter Kit

https://github.com/rahulsuresh-git/cloudflare-worker-gemini-starter-kit

Harness Google Gemini AI's power with a no-cost scalable backend API, and all the benefits of Cloudflare's AI Gateway! Comes with instant setup, DDOS protection, built-in rate limiting, and efficient caching—all in just one click.

This starter kit helps you deploy a backend endpoint for Google Gemini AI through Cloudflare's serverless infrastructure.

#### Example Usage

Input

```
curl 'https://<your-cloudflare-worker-url>/?prompt=What%20is%20life?'
```

Output

```
{
    "success": true,
    "response": "\"Life\" is a complex and multifaceted concept that has been pondered by philosophers, scientists."
}
```

## Features

✅ Serverless (No downtime!) \
✅ Free-of-cost (No Credit Card - perfect for hackathons and developers!) \
✅ Large context and token limit! \
✅ DDOS Protection! \
✅ Rate Limiting! \
✅ Real-time logs! \
✅ Caching! \
✅ Secure!

## Why do we need this?

The rise of Generative AI tools has created a demand for quick and easy access to Large Language Models (LLMs) for developers and students building applications. However, existing solutions often present several challenges. These include credit card requirements for API sign-ups, significant effort needed to host a backend proxy endpoint, backends (like Node.js, Python) requiring additional hosting solutions, and the need for manual implementation of rate-limiting and security mechanisms to prevent abuse.

This starter kit addresses these common problems by leveraging Cloudflare Workers. It is a cloud-based backend server that offers auto-scaling capabilities, and is backed by Cloudflare's leading security features. Best of all, it's completely free to use.

## Deployment

- Create a Cloudflare account. If you don't already have one, sign up for a Cloudflare account at https://www.cloudflare.com

- Get a Google Gemini API key

  - Visit the Google AI Studio at https://aistudio.google.com/app/apikey
  - Accept the consent form
  - Click "Create API key"
  - Select "Create API key in new project"
  - Copy and securely store the generated API key for later use.

- Deploy to Cloudflare by clicking the button below.

  [![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/rahulsuresh-git/cloudflare-worker-gemini-starter-kit)

- After successfully deploying your worker, update its environment variables:

  - Navigate to the Cloudflare Dashboard: dash.cloudflare.com
  - Go to Workers & Pages
  - Select the `cloudflare-worker-gemini-starter-kit` worker
  - Click on Settings > Variables

  - Update the following variables:

  ```
  GOOGLE_GEMINI_API_KEY: Enter your Google Gemini API key

  CLOUDFLARE_ACCOUNT_ID: Find this on the "Workers & Pages" page (right side)

  CLOUDFLARE_AI_GATEWAY_NAME:
      - Go to AI > AI Gateway in the Cloudflare Dashboard
      - Create a new AI Gateway with any name you choose
      - Update this variable with the chosen name
  ```

- Deploy your worker again to apply the changes.

- Test your API by running `curl 'https://<your-cloudflare-worker-url>/?prompt=What%20is%20life?' ` on your terminal. You should see the response from Gemini! 🎉

- Configure rate limiting and caching on the Cloudflare AI Gateway dashboard.

## Run Locally

Clone the project

```bash
  git clone https://github.com/rahulsuresh-git/cloudflare-worker-gemini-starter-kit
```

Go to the project directory

```bash
  cd cloudflare-worker-gemini-starter-kit
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm run dev
```

<!-- ## FAQ

#### Question 1

Answer 1

#### Question 2

Answer 2 -->

## Authors

- [@rahulsuresh-git](https://www.github.com/rahulsuresh-git)

## Disclaimer

Gemini and Cloudflare are separate entities and trademarks of their respective owners. This project is not officially affiliated with, endorsed by, or connected to Gemini or Cloudflare. The Gemini AI service used in this project is provided by Google and is not affiliated with or endorsed by Cloudflare, which serves solely as a backend proxy API for requests. Users must use AI responsibly, considering ethical implications, potential biases, and data privacy. AI-generated content may contain inaccuracies, and users should verify important information from authoritative sources. This starter kit is provided "as is" without warranties, and users are responsible for complying with both Google's and Cloudflare's terms of service. As AI is an evolving technology, users should stay informed about updates and ensure their usage complies with applicable laws and ethical standards. This solution is primarily intended for educational and developmental purposes, and commercial use may require additional considerations. Users are reminded to exercise caution, critical thinking, and responsible practices when utilizing AI technologies.

## License

[MIT](https://choosealicense.com/licenses/mit/)
