# Remote Work Chat

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Remote Work Chat is a lightweight Slack-style collaboration tool built with Next.js and Convex. It helps distributed teams stay connected through realtime channels, direct messages, and emoji reactions. The project showcases how to combine a modern React stack with the Convex backend to create a fast and extensible SaaS foundation.

## Table of Contents

- [Features](#features)
- [Demo](#demo)
- [Setup](#setup)
  - [Simple Mode Setup](#simple-mode-setup)
  - [Advanced Mode Setup](#advanced-mode-setup)
- [Usage](#usage)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [FAQ](#faq)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

## Features

- Authenticate users via password, GitHub, or Google
- Create and manage multiple workspaces with join codes
- Organize conversations in channels or direct messages
- Send rich‑text messages with optional image uploads
- React to messages with emojis in real time
- Edit or delete your own messages with confirmation prompts
- Responsive UI built with Radix UI and Tailwind CSS
- Built‑in toast notifications and modals for a smooth UX

## Demo

A demo of the app running locally:

```
npm run dev
```

If you have a public demo, add the link here.

## Setup

Both simple and advanced setup paths are provided. Ensure you have Node.js installed.

### Simple Mode Setup

1. **Clone the Repository**
   ```bash
   git clone [repo-url]
   cd remote-work
   ```

2. **Install Dependencies**

   ```bash
   npm install
   ```

3. **Configure Environment**

   ```bash
   cp .env.example .env.local
   ```

   Required variables:

   * `NEXT_PUBLIC_CONVEX_URL=` – URL of your Convex deployment
   * `CONVEX_SITE_URL=` – domain used for authentication callbacks
   * `GITHUB_CLIENT_ID=` and `GITHUB_CLIENT_SECRET=`
   * `GOOGLE_CLIENT_ID=` and `GOOGLE_CLIENT_SECRET=`

4. **Run the App**

   ```bash
   npm run dev
   ```

### Advanced Mode Setup

For production or self‑hosted deployments, configure your own Convex backend and OAuth provider secrets. Update the environment variables above with your production values and build the app:

```bash
npm run build
npm start
```

## Usage

1. Sign up or log in using email, GitHub, or Google.
2. Create a workspace or join an existing one using a join code.
3. Add channels to organize discussions or start direct messages with teammates.
4. Post messages, upload images, and react with emojis.
5. Manage workspace settings from the sidebar toolbar.

## Deployment

Deploy to Vercel or your preferred host. The project works out of the box with Vercel.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=remote-work)

1. Set the environment variables in your Vercel dashboard.
2. Push your repository and trigger a deployment.

## Contributing

Contributions are welcome! Fork the repo and open a pull request. Please follow the established code style and check for linting errors before submitting. See `CONTRIBUTING.md` if present.

## FAQ

**How do I get a Convex URL?**
Create a project at [convex.dev](https://www.convex.dev/) and copy the deployment URL into `NEXT_PUBLIC_CONVEX_URL`.

**Can I use other OAuth providers?**
Yes. Update `convex/auth.ts` with additional providers and include their credentials in the `.env.local` file.

**Is this production ready?**
This repo is a starter for building a Slack‑style app. Review the code and security practices before using in production.

## License

This project is licensed under the MIT license.

## Acknowledgements

- [Next.js](https://nextjs.org/)
- [Convex](https://www.convex.dev/)
- [Radix UI](https://www.radix-ui.com/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Jotai](https://jotai.org/)
- [Quill](https://quilljs.com/)

## Contact

For support or questions, please open an issue on the repository.
