# JSunrise Marketing Website
Next.js 14 · TypeScript · Tailwind · Supabase (DB, Auth, Storage)

## Setup
1. `npm install`
2. Create a Supabase project → SQL Editor → run `supabase/schema.sql`.
3. Supabase → Authentication → Users → **Add user** (your admin email/password). Disable public sign-ups in Auth settings.
4. `cp .env.example .env.local` and fill in URL + anon key (the anon key is public by design; never use the service-role key here).
5. `npm run dev`, open `/admin`, sign in, then **Settings → upload the original store photo** (the ONE hero photo) and fill in contact info/business text.

## Security
All writes (products, settings, uploads, reading/deleting inquiries) are restricted by Row Level Security to authenticated users. The public can only read content and insert inquiries.

## Deploy
Push to GitHub → import in Vercel → add the two env vars → Deploy.

## Notes
- One-photo rule: the hero photo is the only image. Save the original from the Google Maps listing yourself and upload it unchanged.
- No business facts are invented; every text field is editable in the admin.


## Upload to GitHub
1. Create a new repository on GitHub.
2. Extract this ZIP file on your computer.
3. Open the extracted `jsunrise` folder and upload its contents (including `app`, `components`, `lib`, `package.json`, and `README.md`) to the repository.
4. In GitHub, choose **Add file → Upload files**, drag the project contents into the page, then click **Commit changes**.
5. To run locally, install Node.js, open a terminal in the project folder, run `npm install`, then `npm run dev`.

Do not upload `.env.local` or any secret keys. Configure the Supabase environment variables in your hosting provider's project settings.
