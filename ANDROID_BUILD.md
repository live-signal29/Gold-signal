# Android build

This project is a Vite/React app packaged for Android with Capacitor 8.

GitHub Actions creates the Android project during the build, so the generated `android/` folder does not need to be committed.

## GitHub Secrets

Add these repository secrets before running the Android workflow:

- `VITE_SUPABASE_PROJECT_ID`
- `VITE_SUPABASE_PUBLISHABLE_KEY`
- `VITE_SUPABASE_URL`
- `VITE_ONESIGNAL_APP_ID`

The workflow creates `.env` only on the GitHub runner.

## Outputs

- Debug APK: installable test build.
- Release APK: unsigned release APK.
- Release AAB: unsigned release bundle for further signing/Play Console upload.

For a Play Store-ready signed APK/AAB, add an Android keystore and GitHub Actions signing secrets.
