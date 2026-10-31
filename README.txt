LUNGE SWAP - source files (Fabric, Minecraft Java 26.2)

BUILD SETUP (26.x is unobfuscated, so the setup differs from older versions)
1. Get the template from https://fabricmc.net/develop for 26.2 (mod id "lungeswap",
   package "com.lungeswap"). It already uses Java 25, Loom plugin
   'net.fabricmc.fabric-loom' and has NO mappings line.
2. Copy this zip's src/ over the template's src/ (replace fabric.mod.json, delete
   the template's example classes/mixins).
3. In build.gradle dependencies { } add (use plain compileOnly, NOT modCompileOnly):
       compileOnly "com.terraformersmc:modmenu:<version for 26.2>"
   Find the version at https://modrinth.com/mod/modmenu
4. Push to GitHub; the template's .github/workflows/build.yml builds it.
   Download the jar (without -sources) from the run's Artifacts.

USE
- Needs Fabric Loader + Fabric API (+ Mod Menu for the settings screen), Java 25.
- Controls -> "Lunge Swap" to bind the key (default R).
- Mod Menu -> Lunge Swap -> config: delay 5-100 ticks, hold/toggle, spear click on/off.
