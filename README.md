# Modlinks
Links to mods for MIO. (FOR MY OWN LOCAL TESTING)

Fields:
```js
export interface Mod {
  id: string; // A UUID used for identifying your mod. You can generate one at https://www.uuidgenerator.net/version4
  slug: string; // The slug from the URL of your github repository. Used for linking to the repository.
  displayTitle: string; // How you want the title of your mod to be displayed.
  author: string; // Your github username, or however you want to be identified. (Used for linking to the github repository, so I'd recommend your github username.)
  description: string; // A short description of your mod.
  versions: Versions; // A list of downloads for your mod. See below.
  configFiles: string[]; // A list of paths that your mod uses inside MIO/modconfig. For example, if your mod uses `modconfig/noclip/keybinds.txt`, you would put `"configFiles": ["noclip/keybinds.txt"]`.
  dependencies: string[]; // A list of UUIDs of mods your mod depends on. You don't have to put Modding API.
}

export type Versions = Record<string, string>; // Used to list versions of your mod and the corresponding .dll file downloads. Example: "versions": {"0.1.0": "https://github.com/YourUsername123/your-mod/releases/download/v0.1.0/your_mod.dll"}
```