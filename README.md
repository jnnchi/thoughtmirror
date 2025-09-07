# ThoughtMirror

![ThoughtMirror Header](placeholder.png)

🏆 **1st Place Winner at GenAI Genesis, Canada's Largest AI Hackathon (600+ hackers)** 🏆

ThoughtMirror is an AI-powered journaling companion that helps users identify and reframe cognitive distortions in real-time. It acts as a gentle guide for self-reflection, empowering users to understand their thought patterns, break free from negative cycles, and foster personal growth without judgment.

## Overview

Journaling is a powerful tool for self-reflection, but it's easy to get stuck in negative thought patterns without realizing it. These patterns, known as cognitive distortions, can subtly shape our reality, leading to anxiety and self-doubt.

ThoughtMirror addresses this by analyzing journal entries as you write. It detects cognitive distortions and provides gentle, therapist-inspired feedback to help you recognize and re-evaluate your thoughts. With an interactive calendar, you can track your emotional patterns over time, gaining clarity and building mental resilience. Our goal is to provide a tool that empowers you to be in control of your own growth and self-discovery.

## How It Works

We replicate a therapeutic approach in a digital format, using a two-stage AI pipeline to provide feedback. The application is built with a modern web stack, featuring a Next.js frontend and a FastAPI backend.

1.  **Distortion Identification (Fine-Tuning)**: We fine-tuned a `Gemini-2.0-Flash-001` model on over 2,000 clinician-annotated text samples. This specialized model accurately identifies and classifies cognitive distortions within a user's journal entry.

2.  **Reflective Prompt Generation (RAG)**: After a distortion is identified, a RAG (Retrieval-Augmented Generation) pipeline using a non-fine-tuned Gemini 2.0 model takes over. It retrieves authentic therapist responses from a curated knowledge base and generates gentle, reflective prompts. This encourages users to think critically about their thought patterns, much like a therapist would.

The backend, built with **FastAPI**, handles the AI processing, user authentication, and data persistence with **Firebase**. The frontend is a responsive **Next.js** application built with **TypeScript** and React, providing a seamless and intuitive user experience.

## Tech Stack

| Area      | Technologies                               |
| :-------- | :----------------------------------------- |
| **Frontend**  | React, Next.js, TypeScript, CSS            |
| **Backend**   | Python, FastAPI                            |
| **AI/ML**     | Google Gemini, LangChain, RAG              |
| **Database**  | Firebase (Firestore)                       |

## Key Features

-   **Real-Time Analysis**: Get instant feedback on your journal entries as you type.
-   **Cognitive Distortion Detection**: Identifies common distortions like catastrophizing, black-and-white thinking, and more.
-   **Therapist-Inspired Feedback**: Receive gentle, non-judgmental prompts to encourage self-reflection.
-   **Interactive Calendar**: Visualize and track your emotional patterns and growth over time.
-   **Secure Journaling**: User data is securely managed using Firebase authentication and storage.

## Gallery

*Homepage*
![ThoughtMirror Homepage](homepage.gif)

*Journaling Page with AI Feedback*
![ThoughtMirror Writing Page](writing_page.gif)

## Future Development

We plan to enhance ThoughtMirror by refining the AI's suggestions with more source data for our RAG implementation. We also aim to build a more interactive dashboard where users can set personalized goals, track emotional patterns with greater detail, and receive more targeted feedback to empower their mental health journey.
