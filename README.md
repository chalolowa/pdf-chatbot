# PDF CHATBOT :wink:
This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).
The user can upload any PDFs he/she likes on the app, and the AI will learn the contents of that PDF file, allowing him/her to ask it questions about that file.

## Prerequisites
You need an OpenAI API Key to build this application.

Also head on over to https://pinecone.io/ and sign up for a free-tier starter account.
Once you’re signed in, click the Create Index button on the Pinecone Dashboard:
1. Set Index Name to be whatever you like - I called mine pdf-chatbot
2. Set Dimensions to be equal to 1536 - this is something specific to OpenAI models. Other AI models may have a different value requirement for Dimensions.
Then click Create Index again and wait for it to be provisioned.

## Getting Started

First install the dependencies:

```bash
npm install
# or
yarn install
```

Second, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Packages Used

1. langchain: For combining our Pinecone vectorstore with OpenAI’s GPT models with ease

2. pdf-parse: Needed by Langchain’s PDF Loader so it can properly parse PDF files

3. ai: Vercel’s new AI SDK which simplifies the task of creating a frontend for Q&A chatbots

4. react-dropzone: For a cool drag-and-drop PDF uploader on our frontend

5. @pinecone-database/pinecone: For communicating with our Pinecone Index