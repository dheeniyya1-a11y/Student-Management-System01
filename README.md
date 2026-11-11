# Al-Dheeniyya Records Management

This is a GitHub Pages deployment copy of the uploaded Al-Dheeniyya Records Management website.

## Upload to GitHub

1. Download and extract `al-dheeniyya-github.zip`.
2. Create a new GitHub repository, for example `al-dheeniyya-records`.
3. Upload `index.html`, `README.md`, and `.nojekyll` to the repository root.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, select **Deploy from a branch**.
6. Choose branch **main** and folder **/(root)**, then save.
7. Wait for GitHub Pages to publish the site. Open the URL shown in the Pages settings.

## Supabase connection

The HTML retains the Supabase project URL and browser-safe publishable key already configured in the uploaded file. It loads the Supabase JavaScript v2 client from jsDelivr.

Before publishing, verify in Supabase that:
- Row Level Security (RLS) is enabled on every table used by the app.
- Policies restrict access to the correct authenticated users and roles.
- Storage bucket policies restrict access to private student/staff documents.
- No `service_role` key or other secret is placed in this repository.

## Privacy cleanup performed

The uploaded HTML contained embedded student and staff records, phone numbers, document references/notes and profile photos. Those embedded records and photos have been removed from this GitHub copy. The app is configured to load live records from Supabase after a successful sign-in.

The original uploaded file has not been changed.

## Important

GitHub Pages is static hosting. The app can still communicate with Supabase from the browser, provided the Supabase project, authentication, RLS policies and storage permissions are correctly configured. Publishing this repository does not create or configure those backend resources.
