# Slime Rancher — Minecraft Java 1.21.1 + Fabric

This is a source project, not a precompiled JAR. It contains basic Slime Rancher-inspired mechanics: a vacpack/capsule capture flow, feeding slimes for plorts, and a craftable corral block. The slime variants currently reuse vanilla slime entities and differ mainly by size/name.

## Build the JAR on Windows 11 (no local Gradle install required)

This project includes a GitHub Actions workflow. GitHub's build runner installs Java 21 and Gradle, then compiles the mod and publishes the JAR as a downloadable build artifact.

1. Unzip the project.
2. Create a repository on GitHub and upload all files/folders from this project.
3. Open the repository's **Actions** tab and allow workflows if prompted.
4. Run **Build Fabric mod JAR** (or push a commit to the main branch).
5. Open the completed workflow run, find **Artifacts**, and download `slime-rancher-1.21.1`.
6. Unzip the artifact and copy the `.jar` into `%appdata%\.minecraft\mods` alongside Fabric Loader and Fabric API for Minecraft 1.21.1.

## Notes

I could not compile or launch Minecraft in this environment because Gradle is not installed and outbound network access is unavailable. The GitHub workflow is included to perform a real build remotely; if the first build reports API errors, those must be fixed before the JAR can be considered working. Back up worlds before testing mods.
