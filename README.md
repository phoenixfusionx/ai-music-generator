# AI Music Generator

<p align="center">
  <img src="./public/logo.png" alt="AI Music Generator Logo"/>
</p>

AI Music Generator is a web application built with [Next.js](https://nextjs.org/) that leverages [Suno AI](https://suno.com/) to generate music tracks using artificial intelligence.

> **Note:** The example site may not always be able to generate music due to potential expiration of the required Suno cookie. To resolve this, deploy your own instance and update the `SUNO_COOKIE` environment variable. If issues persist, refer to [suno-api](https://github.com/gcui-art/suno-api) for troubleshooting.

## Getting Started

### Prerequisites

- A [Suno AI](https://suno.com) account and its session cookie
- Node.js and npm installed
- A PostgreSQL database

### 1. Obtain Suno AI Cookie

1. Log in to your [Suno AI](https://suno.com) account.
2. Locate a network request containing the keyword `client?_clerk_js_version`.
3. In the request details, navigate to the **Cookie** section and copy the entire cookie value.

### 2. Clone the Repository

```bash
git clone https://github.com/phoenixfusionx/ai-music-generator.git
cd ai-music-generator
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Initialize the Database

1. Create your PostgreSQL database.
2. Run the following commands to set up the schema and seed initial data:

```bash
npm run db:push
npm run db:seed
```

> **Note:** Data is seeded by crawling the Suno API via the official website. This method may be subject to change if the API is updated.

### 5. Configure Environment Variables

Create a `.env` file in the project root with the following variables:

```
SUNO_COOKIE=your_suno_cookie_here

POSTGRES_PRISMA_URL=your_postgres_prisma_url

POSTGRES_URL_NON_POOLING=your_postgres_url_non_pooling

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key

CLERK_SECRET_KEY=your_clerk_secret_key

NEXT_PUBLIC_URL=your_public_url

LEMONSQUEEZY_API_KEY=your_lemonsqueezy_api_key

LEMONSQUEEZY_STORE_ID=your_lemonsqueezy_store_id

LEMONSQUEEZY_PRODUCT_ID=your_lemonsqueezy_product_id

LEMONSQUEEZY_WEBHOOK_SECRET=your_lemonsqueezy_webhook_secret
```

### 6. Start the Development Server

```bash
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000) in your browser to access the application.

## Acknowledgements

- [Suno AI](https://suno.com)
- [Next.js](https://nextjs.org)
- [Tailwind CSS](https://tailwindcss.com)
- [Clerk](https://clerk.com)
- [Lemonsqueezy](https://www.lemonsqueezy.com)
- [shadcn/ui](https://ui.shadcn.com/)
- [Prisma](https://www.prisma.io/orm)
- [suno-api](https://github.com/gcui-art/suno-api)

## Author

Developed and maintained by [PhoenixFusionX](https://github.com/phoenixfusionx). For questions or contributions, please open an issue or submit a pull request.
