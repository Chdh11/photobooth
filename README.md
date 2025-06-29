# Photobooth App

![Next.js](https://img.shields.io/badge/Next.js-15.3.4-black?logo=nextdotjs)
![Supabase](https://img.shields.io/badge/Supabase-Enabled-3ECF8E?logo=supabase)
![License](https://img.shields.io/github/license/your-username/your-repo-name)
![Status](https://img.shields.io/badge/status-In%20Progress-yellow)

A web-based photobooth where users can snap photos, create photostrips, add messages, and store them month-wise — all protected by authentication and backed by Supabase.

---

## Features

- Camera Integration – Take 3 quick selfies with countdown and filters.
- Photostrip Generator – Automatically combines photos into a vertical strip.
- Custom Messages – Add a personal note with every photostrip.
- Supabase Storage – Saves images and metadata securely.
- User Authentication – Users get their own private galleries.
- Month-wise Folders – Organizes photostrips by creation month.

---

## Technologies Used

- Frontend: Next.js 15 (App Router), Tailwind CSS
- Backend: Supabase (Auth, Storage, Postgres DB)
- Image Handling: HTML5 Canvas, `<video>`, Blob uploads
- Authentication: Supabase SSR, cookie-based sessions

---

## Database Schema

**Table: `photos`**
| Column      | Type     | Description                         |
|-------------|----------|-------------------------------------|
| `id`        | integer  | Auto-increment primary key          |
| `user_id`   | uuid     | Linked to Supabase auth user ID     |
| `image_url` | text     | Path to Supabase storage image      |
| `message`   | text     | Optional user message               |
| `created_at`| timestamp| Auto-generated timestamp            |

**Bucket: `photostrips`**
- Stores JPEG photostrip files uploaded via canvas.

---

## Concepts Learned

- Supabase integration (Auth, Database, Storage)
- Server Actions with Next.js App Router
- Canvas-based image capture and manipulation
- Middleware and SSR session handling with Supabase
- UI filtering by user and month
- Organizing and retrieving user-specific files

---

Made by Chhavi Dhankhar
