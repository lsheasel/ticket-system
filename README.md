# 🎫 Ticket System

A simple ticket management system built with [React](https://reactjs.org/), [Vite](https://vitejs.dev/), [TailwindCSS](https://tailwindcss.com/), and [Supabase](https://supabase.com/).

## 🚀 Features

- User registration and login (Supabase Auth)
- Create, view, and update tickets
- Real-time database using Supabase
- Responsive UI with TailwindCSS
- Optional admin/user roles

## 🛠️ Tech Stack

- ⚛️ React (with Vite)
- 💨 TailwindCSS
- 🧰 Supabase (Auth & Database)
- 📦 Zustand or React Context (for global state management)

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/your-username/ticket-system.git
cd ticket-system

# Install dependencies
npm install

# Start local development server
npm run dev
````

## ⚙️ Configuration

1. Create a project at [supabase.com](https://supabase.com/)
2. Set up your database tables (e.g., `tickets`, `users`)
3. Add your Supabase keys to a `.env` file in the root:

```env
VITE_SUPABASE_URL=your-supabase-url
VITE_SUPABASE_ANON_KEY=your-anon-key
```

4. Example SQL schema for a `tickets` table:

```sql
create table tickets (
  id uuid primary key default uuid_generate_v4(),
  title text not null,
  description text,
  status text default 'open',
  user_id uuid references auth.users,
  created_at timestamp default now()
);
```

## 📁 Project Structure

```
src/
├── components/
├── pages/
├── hooks/
├── lib/
│   └── supabaseClient.js
├── App.jsx
└── main.jsx
```

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to change.

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

> Built with ❤️ by Shease
