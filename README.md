
Format: HTML
max tokens
50000

All Extensions

Base path: root
±7908 tokens


Copy
├── .gitignore
├── .nvmrc
├── .vscode
    ├── extensions.json
    └── launch.json
├── README.md
├── astro.config.mjs
├── bun.lockb
├── package-lock.json
├── package.json
├── public
    └── favicon.svg
├── src
    ├── components
    │   ├── DotsButton.astro
    │   ├── GreetingTitle.svelte
    │   ├── InlineArtists.astro
    │   ├── LikeButton.astro
    │   ├── MusicsTable.astro
    │   ├── PageHeader.astro
    │   ├── PlayButton.astro
    │   ├── PlaylistCard.astro
    │   ├── PlaylistItemCard.astro
    │   ├── PureInlineArtists.astro
    │   └── Side
    │   │   ├── SideItemCard.astro
    │   │   ├── SideMenu.astro
    │   │   └── SideMenuItem.astro
    ├── env.d.ts
    ├── layouts
    │   ├── Layout.astro
    │   └── layout.css
    ├── lib
    │   ├── colors.ts
    │   └── data.ts
    └── pages
    │   ├── index.astro
    │   └── playlist
    │       └── [id].astro
├── svelte.config.js
├── tailwind.config.cjs
└── tsconfig.json


/.gitignore:
--------------------------------------------------------------------------------
 1 | # build output
 2 | dist/
 3 | 
 4 | # generated types
 5 | .astro/
 6 | 
 7 | # dependencies
 8 | node_modules/
 9 | ./dhvani
10 | 
11 | # logs
12 | npm-debug.log*
13 | yarn-debug.log*
14 | yarn-error.log*
15 | pnpm-debug.log*
16 | 
17 | # environment variables
18 | .env
19 | .env.production
20 | 
21 | # macOS-specific files
22 | .DS_Store
23 | 


--------------------------------------------------------------------------------
/.nvmrc:
--------------------------------------------------------------------------------
1 | v18


--------------------------------------------------------------------------------
/.vscode/extensions.json:
--------------------------------------------------------------------------------
1 | {
2 |   "recommendations": ["astro-build.astro-vscode"],
3 |   "unwantedRecommendations": []
4 | }
5 | 


--------------------------------------------------------------------------------
/.vscode/launch.json:
--------------------------------------------------------------------------------
 1 | {
 2 |   "version": "0.2.0",
 3 |   "configurations": [
 4 |     {
 5 |       "command": "./node_modules/.bin/astro dev",
 6 |       "name": "Development server",
 7 |       "request": "launch",
 8 |       "type": "node-terminal"
 9 |     }
10 |   ]
11 | }
12 | 


--------------------------------------------------------------------------------
/README.md:
--------------------------------------------------------------------------------
 1 | # Spotify clone with View Transitions from Astro 3.0 [![Built with Astro](https://astro.badg.es/v2/built-with-astro/tiny.svg)](https://astro.build)
 2 | 
 3 | Clone of Spotify with [Astro View Transitions](https://docs.astro.build/en/guides/view-transitions/) is an **experimental feature** for fluid navigation, this example use tailwindcss and svelte.
 4 | 
 5 | ### About
 6 | 
 7 | View Transition is a **experimental** mechanism to transition between DOM states, learn more in these links:
 8 | 
 9 | - Astro Documentation: https://docs.astro.build/en/guides/view-transitions/
10 | - MDN Documentation: https://developer.mozilla.org/en-US/docs/Web/API/View_Transitions_API


--------------------------------------------------------------------------------
/astro.config.mjs:
--------------------------------------------------------------------------------
 1 | import { defineConfig } from "astro/config";
 2 | import tailwind from "@astrojs/tailwind";
 3 | 
 4 | import svelte from "@astrojs/svelte";
 5 | 
 6 | // https://astro.build/config
 7 | export default defineConfig({
 8 |   root: "./src",
 9 |   integrations: [tailwind(), svelte()],
10 | });
11 | 


--------------------------------------------------------------------------------
/bun.lockb:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/the-bipu/spotify-astro-theme/main/bun.lockb


--------------------------------------------------------------------------------
/package.json:
--------------------------------------------------------------------------------
 1 | {
 2 |   "name": "spotify-astro-transitions",
 3 |   "description": "Clone of Spotify with Astro View Transitions integration for fluid navigation",
 4 |   "type": "module",
 5 |   "version": "0.0.1",
 6 |   "author": "https://github.com/igorm84",
 7 |   "scripts": {
 8 |     "dev": "astro dev",
 9 |     "start": "astro dev",
10 |     "build": "astro build",
11 |     "preview": "astro preview",
12 |     "astro": "astro"
13 |   },
14 |   "dependencies": {
15 |     "@astrojs/svelte": "^4.0.0",
16 |     "@astrojs/tailwind": "^5.0.0",
17 |     "astro": "^3.0.7",
18 |     "astro-icon": "^0.8.1",
19 |     "svelte": "^4.0.0",
20 |     "tailwindcss": "^3.0.24"
21 |   },
22 |   "devDependencies": {
23 |     "@tailwindcss/typography": "^0.5.9",
24 |     "prettier": "^3.0.3",
25 |     "prettier-plugin-astro": "^0.12.0",
26 |     "prettier-plugin-tailwindcss": "^0.5.4"
27 |   }
28 | }
29 | 


--------------------------------------------------------------------------------
/public/favicon.svg:
--------------------------------------------------------------------------------
 1 | <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 128 128">
 2 |     <path d="M50.4 78.5a75.1 75.1 0 0 0-28.5 6.9l24.2-65.7c.7-2 1.9-3.2 3.4-3.2h29c1.5 0 2.7 1.2 3.4 3.2l24.2 65.7s-11.6-7-28.5-7L67 45.5c-.4-1.7-1.6-2.8-2.9-2.8-1.3 0-2.5 1.1-2.9 2.7L50.4 78.5Zm-1.1 28.2Zm-4.2-20.2c-2 6.6-.6 15.8 4.2 20.2a17.5 17.5 0 0 1 .2-.7 5.5 5.5 0 0 1 5.7-4.5c2.8.1 4.3 1.5 4.7 4.7.2 1.1.2 2.3.2 3.5v.4c0 2.7.7 5.2 2.2 7.4a13 13 0 0 0 5.7 4.9v-.3l-.2-.3c-1.8-5.6-.5-9.5 4.4-12.8l1.5-1a73 73 0 0 0 3.2-2.2 16 16 0 0 0 6.8-11.4c.3-2 .1-4-.6-6l-.8.6-1.6 1a37 37 0 0 1-22.4 2.7c-5-.7-9.7-2-13.2-6.2Z" />
 3 |     <style>
 4 |         path { fill: #000; }
 5 |         @media (prefers-color-scheme: dark) {
 6 |             path { fill: #FFF; }
 7 |         }
 8 |     </style>
 9 | </svg>
10 | 


--------------------------------------------------------------------------------
/src/components/DotsButton.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | import Icon from "astro-icon";
 3 | 
 4 | interface Props {
 5 |   size?: "md" | "lg";
 6 | }
 7 | 
 8 | const { size = "md" } = Astro.props;
 9 | ---
10 | 
11 | <button
12 |   type="button"
13 |   class="text-gray-400 hover:text-gray-300 rounded-full flex items-center justify-center"
14 |   class:list={[size === "md" && "h-12 w-12", size === "lg" && "h-14 w-14"]}
15 | >
16 |   <Icon
17 |     name="tabler:dots"
18 |     class:list={[size === "md" && "h-8 w-8", size === "lg" && "h-8 w-8"]}
19 |   />
20 | </button>
21 | 


--------------------------------------------------------------------------------
/src/components/GreetingTitle.svelte:
--------------------------------------------------------------------------------
 1 | <script lang="ts">
 2 |   const currentTime = new Date();
 3 |   const currentHour = currentTime.getHours();
 4 | 
 5 |   let greeting = "";
 6 | 
 7 |   if (currentHour >= 5 && currentHour < 12) {
 8 |     greeting = "Good morning";
 9 |   } else if (currentHour >= 12 && currentHour < 18) {
10 |     greeting = "Good afternoon";
11 |   } else {
12 |     greeting = "Good night";
13 |   }
14 | </script>
15 | 
16 | <h1 class="text-3xl font-bold">{greeting}</h1>
17 | 


--------------------------------------------------------------------------------
/src/components/InlineArtists.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | interface Props {
 3 |   artists: string[];
 4 | }
 5 | 
 6 | const { artists } = Astro.props;
 7 | ---
 8 | 
 9 | {
10 |   artists.map((artist, index) => {
11 |     return (
12 |       <>
13 |         <a href={"#"} class="hover:underline">
14 |           {artist}
15 |         </a>
16 |         <span class="text-gray-300">
17 |           {index === artists.length - 1 ? " " : ", "}
18 |         </span>
19 |       </>
20 |     );
21 |   })
22 | }
23 | 


--------------------------------------------------------------------------------
/src/components/LikeButton.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | import Icon from "astro-icon";
 3 | 
 4 | interface Props {
 5 |   size?: "md" | "lg";
 6 | }
 7 | 
 8 | const { size = "md" } = Astro.props;
 9 | ---
10 | 
11 | <button
12 |   type="button"
13 |   class="text-green-500 hover:scale-105 rounded-full flex items-center justify-center"
14 |   class:list={[size === "md" && "h-12 w-12", size === "lg" && "h-14 w-14"]}
15 | >
16 |   <Icon
17 |     name="mdi:heart"
18 |     class:list={[size === "md" && "h-8 w-8", size === "lg" && "h-10 w-10"]}
19 |   />
20 | </button>
21 | 


--------------------------------------------------------------------------------
/src/components/MusicsTable.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | import { Icon } from "astro-icon";
 3 | import { songs } from "../lib/data";
 4 | import PureInlineArtists from "./PureInlineArtists.astro";
 5 | import InlineArtists from "./InlineArtists.astro";
 6 | ---
 7 | 
 8 | <table class="table-auto text-left min-w-full divide-y-2 divide-gray-500/30">
 9 |   <thead>
10 |     <tr class="text-gray-300">
11 |       <th class="font-normal px-4 py-2 whitespace-nowrap">#</th>
12 |       <th class="font-normal px-4 py-2 whitespace-nowrap">Title</th>
13 |       <th class="font-normal px-4 py-2 whitespace-nowrap">Album</th>
14 |       <th class="font-normal px-4 py-2 whitespace-nowrap text-right">
15 |         <Icon name="carbon:time" class="inline-block h-5 w-5" />
16 |       </th>
17 |     </tr>
18 |   </thead>
19 |   <tbody>
20 |     {
21 |       songs.map((song, index) => (
22 |         <tr class="group hover:bg-gray-500/20">
23 |           <td class="whitespace-nowrap px-4 py-2">{index + 1}</td>
24 |           <td class="whitespace-nowrap px-4 py-2 flex gap-3 items-center">
25 |             <div class="h-10 w-10">
26 |               <img
27 |                 src={song.image}
28 |                 alt={song.title}
29 |                 class="rounded object-cover h-full w-full shadow-[5px_0_30px_0px_rgba(0,0,0,0.3)]"
30 |               />
31 |             </div>
32 |             <div class="leading-none">
33 |               <a
34 |                 href="#"
35 |                 class="text-gray-300 group-hover:text-white hover:underline text-sm"
36 |               >
37 |                 {song.title}
38 |               </a>
39 |               <div class="text-sm text-gray-300 group-hover:text-white">
40 |                 <InlineArtists artists={song.artists} />
41 |               </div>
42 |             </div>
43 |           </td>
44 |           <td class="whitespace-nowrap px-4 py-2">
45 |             <a
46 |               href="#"
47 |               class="text-gray-300 group-hover:text-white hover:underline text-sm"
48 |             >
49 |               {song.album}
50 |             </a>
51 |           </td>
52 |           <td class="whitespace-nowrap px-4 py-2 text-right">
53 |             {song.duration}
54 |           </td>
55 |         </tr>
56 |       ))
57 |     }
58 |   </tbody>
59 | </table>
60 | 


--------------------------------------------------------------------------------
/src/components/PageHeader.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | import Icon from "astro-icon";
 3 | ---
 4 | 
 5 | <div
 6 |   class="relative z-10 py-4 px-6 flex justify-between"
 7 |   transition:name="page header"
 8 |   transition:persist
 9 | >
10 |   <a
11 |     href="/"
12 |     aria-label="go back to home page"
13 |     class="bg-zinc-900 rounded-full inline-flex justify-center items-center h-8 w-8"
14 |   >
15 |     <Icon name="bi:chevron-left" class="h-4 w-4 -ml-0.5" />
16 |   </a>
17 |   <div class="flex items-center gap-3">
18 |     <a
19 |       target="_blank"
20 |       href="https://spotify-astro-theme.vercel.app/"
21 |       class="flex relative overflow-hidden group bg-gradient-to-br from-black/10 to-black/40 rounded-md px-2.5 h-7 text-gray-200 hover:text-white transition-colors gap-1 items-center"
22 |     >
23 |       <span class="text-xs">
24 |         View on <span class="font-bold">Vercel</span>
25 |       </span>
26 |       <Icon name="ion:logo-vercel" class="h-4 w-4" />
27 |     </a>
28 |     <a
29 |       target="_blank"
30 |       aria-label={"github repository"}
31 |       href="https://github.com/the-bipu/spotify-astro-theme"
32 |       class="text-gray-200 hover:text-white"
33 |     >
34 |       <Icon name="mdi:github" class="h-7 w-7" />
35 |     </a>
36 |   </div>
37 | </div>
38 | 


--------------------------------------------------------------------------------
/src/components/PlayButton.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | import Icon from "astro-icon";
 3 | 
 4 | interface Props {
 5 |   size?: "md" | "lg";
 6 | }
 7 | 
 8 | const { size = "md" } = Astro.props;
 9 | ---
10 | 
11 | <span
12 |   class="bg-green-500 hover:scale-105 shadow-md shadow-black/40 rounded-full flex items-center justify-center text-black"
13 |   class:list={[size === "md" && "h-12 w-12", size === "lg" && "h-14 w-14"]}
14 | >
15 |   <Icon
16 |     name="mdi:play"
17 |     class:list={[size === "md" && "h-8 w-8", size === "lg" && "h-10 w-10"]}
18 |   />
19 | </span>
20 | 


--------------------------------------------------------------------------------
/src/components/PlaylistCard.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | import type { Playlist } from "../lib/data";
 3 | import PlayButton from "./PlayButton.astro";
 4 | import PureInlineArtists from "./PureInlineArtists.astro";
 5 | interface Props {
 6 |   playlist: Playlist;
 7 | }
 8 | 
 9 | const { playlist } = Astro.props;
10 | ---
11 | 
12 | <a
13 |   href={`/playlist/${playlist.id}`}
14 |   class="playlist-card p-4 flex-col items-center group relative transition-all duration-300 overflow-hidden gap-5 rounded-md shadow-lg hover:shadow-xl outline-none bg-zinc-500/5 hover:bg-zinc-500/20 focus:bg-zinc-500/20"
15 |   data-color={playlist.color.dark}
16 |   transition:name=`playlist ${playlist.id} box`
17 | >
18 |   <div class="w-40">
19 |     <div class="relative group mx-auto h-40 w-full flex-none shadow-lg">
20 |       <img
21 |         src={playlist.cover}
22 |         alt={playlist.title}
23 |         class="object-cover h-full w-full rounded-md shadow-[5px_0_30px_0px_rgba(0,0,0,0.3)]"
24 |         transition:name=`playlist ${playlist.id} image`
25 |       />
26 |       <div
27 |         class="absolute right-2 bottom-2 translate-y-4 group-hover:translate-y-0 opacity-0 group-hover:opacity-100 transition-all"
28 |         transition:name=`playlist ${playlist.id} play`
29 |       >
30 |         <PlayButton />
31 |       </div>
32 |     </div>
33 |     <div class="pt-2">
34 |       <div
35 |         class="font-bold block truncate"
36 |         transition:name=`playlist ${playlist.id} title`
37 |       >
38 |         {playlist.title}
39 |       </div>
40 |       <div class="text-gray-400 text-xs">
41 |         <PureInlineArtists artists={playlist.artists} />
42 |       </div>
43 |     </div>
44 |   </div>
45 | </a>
46 | 


--------------------------------------------------------------------------------
/src/components/PlaylistItemCard.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | import type { Playlist } from "../lib/data";
 3 | import PlayButton from "./PlayButton.astro";
 4 | interface Props {
 5 |   playlist: Playlist;
 6 | }
 7 | 
 8 | const { playlist } = Astro.props;
 9 | ---
10 | 
11 | <a
12 |   href={`/playlist/${playlist.id}`}
13 |   class="playlist-item flex group relative transition-all duration-300 overflow-hidden items-center gap-5 rounded-md shadow-lg hover:shadow-xl outline-none bg-zinc-500/30 hover:bg-zinc-500/50 focus:bg-zinc-500/50"
14 |   data-color={playlist.color.dark}
15 |   transition:name=`playlist ${playlist.id} box`
16 | >
17 |   <div class="h-20 w-20">
18 |     <img
19 |       src={playlist.cover}
20 |       alt={playlist.title}
21 |       class="object-cover h-full w-full shadow-[5px_0_30px_0px_rgba(0,0,0,0.3)]"
22 |       transition:name=`playlist ${playlist.id} image`
23 |     />
24 |   </div>
25 |   <div class="font-bold block" transition:name=`playlist ${playlist.id} title`>
26 |     {playlist.title}
27 |   </div>
28 |   <div
29 |     class={"absolute right-4 opacity-0 group-hover:opacity-100 transition-opacity duration-300"}
30 |     transition:name=`playlist ${playlist.id} play`
31 |   >
32 |     <PlayButton />
33 |   </div>
34 | </a>
35 | 


--------------------------------------------------------------------------------
/src/components/PureInlineArtists.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | interface Props {
 3 |   artists: string[];
 4 | }
 5 | 
 6 | const { artists } = Astro.props;
 7 | ---
 8 | 
 9 | {
10 |   artists.map((artist, index) => (
11 |     <>
12 |       {artist}
13 |       {index === artists.length - 1 ? " " : ", "}
14 |     </>
15 |   ))
16 | }
17 | 


--------------------------------------------------------------------------------
/src/components/Side/SideItemCard.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | import type { Playlist } from "../../lib/data";
 3 | import InlineArtists from "../InlineArtists.astro";
 4 | import PlayButton from "../PlayButton.astro";
 5 | import PureInlineArtists from "../PureInlineArtists.astro";
 6 | interface Props {
 7 |   playlist: Playlist;
 8 | }
 9 | 
10 | const { playlist } = Astro.props;
11 | ---
12 | 
13 | <a
14 |   href={`/playlist/${playlist.id}`}
15 |   class="playlist-item flex group relative p-2 overflow-hidden items-center gap-5 rounded-md shadow-lg hover:shadow-xl outline-none hover:bg-zinc-500/10 focus:bg-zinc-500/50"
16 |   data-color={playlist.color.dark}
17 | >
18 |   <div class="h-12 w-12 flex-none">
19 |     <img
20 |       src={playlist.cover}
21 |       alt={playlist.title}
22 |       class="object-cover rounded h-full w-full shadow-[5px_0_30px_0px_rgba(0,0,0,0.3)]"
23 |     />
24 |   </div>
25 |   <div class="flex flex-auto flex-col truncate">
26 |     <div class="font-semibold w-full flex-none truncate">
27 |       {playlist.title}
28 |     </div>
29 |     <div class="text-gray-400 text-sm truncate flex-1">
30 |       <PureInlineArtists artists={playlist.artists} />
31 |     </div>
32 |   </div>
33 | </a>
34 | 


--------------------------------------------------------------------------------
/src/components/Side/SideMenu.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | import SideMenuItem from "./SideMenuItem.astro";
 3 | import { sidebarPlaylists } from "../../lib/data";
 4 | import SideItemCard from "./SideItemCard.astro";
 5 | ---
 6 | 
 7 | <div class="flex flex-col flex-1 gap-2">
 8 |   <div class="bg-zinc-900 rounded-lg">
 9 |     <ul>
10 |       <SideMenuItem href="/" iconName="carbon:home">Home</SideMenuItem>
11 |       <SideMenuItem href="#" iconName="carbon:search">Search</SideMenuItem>
12 |     </ul>
13 |   </div>
14 | 
15 |   <div class="bg-zinc-900 rounded-lg flex-1">
16 |     <ul>
17 |       <SideMenuItem href="#" iconName="carbon:media-library">
18 |         Your library
19 |       </SideMenuItem>
20 |     </ul>
21 |     <ul class="pl-2">
22 |       {sidebarPlaylists.map((playlist) => <SideItemCard {playlist} />)}
23 |     </ul>
24 |   </div>
25 | </div>
26 | 


--------------------------------------------------------------------------------
/src/components/Side/SideMenuItem.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | import Icon from "astro-icon";
 3 | 
 4 | type Props = {
 5 |   href?: string;
 6 |   iconName?: string;
 7 | };
 8 | 
 9 | const { href, iconName } = Astro.props;
10 | ---
11 | 
12 | <li>
13 |   <a
14 |     {href}
15 |     class="flex gap-4 text-zinc-400 hover:text-zinc-100 py-3.5 px-5 font-semibold transition-all duration-300"
16 |   >
17 |     <Icon name={iconName} class="h-6 w-6" />
18 |     <slot />
19 |   </a>
20 | </li>
21 | 


--------------------------------------------------------------------------------
/src/env.d.ts:
--------------------------------------------------------------------------------
1 | /// <reference types="astro/client" />
2 | 


--------------------------------------------------------------------------------
/src/layouts/Layout.astro:
--------------------------------------------------------------------------------
  1 | ---
  2 | interface Props {
  3 |   title: string;
  4 |   image?: string;
  5 | }
  6 | 
  7 | const {
  8 |   title = "Home",
  9 |   image = "https://res.cloudinary.com/dp3ppkxo5/image/upload/v1693776174/spotify-astro/playlist_2_f9ymlx.jpg",
 10 | } = Astro.props;
 11 | import { ViewTransitions } from "astro:transitions";
 12 | import "./layout.css";
 13 | import SideMenu from "../components/Side/SideMenu.astro";
 14 | ---
 15 | 
 16 | <!doctype html>
 17 | <html lang="en">
 18 |   <head>
 19 |     <meta charset="UTF-8" />
 20 |     <meta
 21 |       name="description"
 22 |       content="Clone of Spotify with Astro View Transitions integration for fluid navigation"
 23 |     />
 24 |     <meta name="viewport" content="width=device-width" />
 25 |     <link rel="icon" type="image/svg+xml" href="/favicon.svg" />
 26 |     <meta name="generator" content={Astro.generator} />
 27 |     <title>{title} | Spotify Astro</title>
 28 |     <meta property="og:image" content={image} />
 29 |     <meta name="twitter:image" content={image} />
 30 |     <ViewTransitions fallback="none" />
 31 |   </head>
 32 |   <body class="dark">
 33 |     <div class="relative h-screen p-2 gap-2 flex items-stretch">
 34 |       <div class="w-[350px] flex-col hidden lg:flex overflow-y-auto">
 35 |         <SideMenu />
 36 |       </div>
 37 |       <div class="rounded-lg bg-zinc-900 flex-1 mx-auto overflow-y-auto">
 38 |         <slot />
 39 |       </div>
 40 |     </div>
 41 |     <div
 42 |       id="not-support"
 43 |       class="fixed hidden bg-red-700 bottom-0 inset-x-0 rounded-t-md text-center py-2 lg:py-4 z-50 font-semibold"
 44 |     >
 45 |       It seems your browser does not support view transitions yet :( try it
 46 |       using chrome or edge <a
 47 |         class="underline"
 48 |         href="https://github.com/igorm84/spotify-astro-transitions"
 49 |         >(see docs here)</a
 50 |       >
 51 |     </div>
 52 |     <script is:inline defer>
 53 |       function setContainerColor(dataColor) {
 54 |         const playlistContainer = document.getElementById("playlist-container");
 55 |         const currentColor = playlistContainer?.getAttribute("data-color");
 56 |         if (dataColor && dataColor !== currentColor) {
 57 |           playlistContainer?.style.setProperty("--context-color", dataColor);
 58 |           playlistContainer?.setAttribute("data-color", dataColor);
 59 |         }
 60 |       }
 61 | 
 62 |       window.coloradTimeout = null;
 63 |       for (const playlist of document.querySelectorAll(".playlist-item")) {
 64 |         playlist.addEventListener("mouseover", () =>
 65 |           onMouseOverColorad(playlist)
 66 |         );
 67 |         playlist.addEventListener("mouseout", onMouseOutColorad);
 68 |         playlist.addEventListener("focus", () => onMouseFocusColorad(playlist));
 69 |         playlist.addEventListener("blur", onMouseOutColorad);
 70 |       }
 71 | 
 72 |       function onMouseFocusColorad(el) {
 73 |         if (el) {
 74 |           const dataColor = el.getAttribute("data-color");
 75 |           if (!dataColor) return;
 76 |           setContainerColor(dataColor);
 77 |         }
 78 |       }
 79 |       function onMouseOverColorad(el) {
 80 |         if (el) {
 81 |           const dataColor = el.getAttribute("data-color");
 82 |           if (!dataColor) return;
 83 |           window.coloradTimeout = setTimeout(
 84 |             () => setContainerColor(dataColor),
 85 |             200
 86 |           );
 87 |         }
 88 |       }
 89 |       function onMouseOutColorad() {
 90 |         if (window.coloradTimeout) {
 91 |           clearTimeout(window.coloradTimeout);
 92 |           window.coloradTimeout = null;
 93 |         }
 94 |       }
 95 |     </script>
 96 |     <script>
 97 |       if (!document.startViewTransition) {
 98 |         document.getElementById("not-support").classList.remove("hidden");
 99 |       }
100 |       document.addEventListener("astro:page-load", () => {
101 |         for (const el of document.querySelectorAll(".el-to-fade")) {
102 |           el.classList.remove("scale-90");
103 |         }
104 |       });
105 |     </script>
106 |   </body>
107 | </html>
108 | 


--------------------------------------------------------------------------------
/src/layouts/layout.css:
--------------------------------------------------------------------------------
 1 | :root {
 2 |   --color-primary: theme(colors.green.500);
 3 |   --color-background: theme(colors.zinc.950);
 4 |   --color-foreground: theme(colors.zinc.900);
 5 | }
 6 | body {
 7 |   background: var(--color-background);
 8 |   color: white;
 9 | }
10 | 
11 | * {
12 |   scrollbar-width: 10px;
13 |   scrollbar-color: rgb(50, 50, 50) rgb(30, 30, 30);
14 | }
15 | *::-webkit-scrollbar {
16 |   height: 10px;
17 |   width: 10px;
18 | }
19 | *::-webkit-scrollbar-track {
20 |   border-radius: 5px;
21 |   background-color: transparent;
22 | }
23 | 
24 | *::-webkit-scrollbar-track:hover {
25 |   background-color: rgb(30, 30, 30);
26 | }
27 | 
28 | *::-webkit-scrollbar-track:active {
29 |   background-color: rgb(30, 30, 30);
30 | }
31 | 
32 | *::-webkit-scrollbar-thumb {
33 |   border-radius: 5px;
34 |   background-color: rgb(50, 50, 50);
35 | }
36 | 
37 | *::-webkit-scrollbar-thumb:hover {
38 |   background-color: rgb(70, 70, 70);
39 | }
40 | 
41 | *::-webkit-scrollbar-thumb:active {
42 |   background-color: rgb(70, 70, 70);
43 | }
44 | 


--------------------------------------------------------------------------------
/src/lib/colors.ts:
--------------------------------------------------------------------------------
 1 | export const colors = {
 2 |   red: { accent: "#da2735", dark: "#7f1d1d" },
 3 |   orange: { accent: "#cc5400", dark: "#7c2d12" },
 4 |   yellow: { accent: "#ffae00", dark: "#78350f" },
 5 |   green: { accent: "#21c872", dark: "#14532d" },
 6 |   teal: { accent: "#2ee9d7", dark: "#134e4a" },
 7 |   blue: { accent: "#1e3a8a", dark: "#1e3a8a" },
 8 |   indigo: { accent: "#394bd5", dark: "#312e81" },
 9 |   purple: { accent: "#df24ff", dark: "#581c87" },
10 |   pink: { accent: "#f33b73", dark: "#831843" },
11 |   emerald: { accent: "#0c6e54", dark: "#064e3b" },
12 |   rose: { accent: "#ed2377", dark: "#871b48" },
13 |   gray: { accent: "#555555", dark: "#27272a" },
14 | };
15 | 


--------------------------------------------------------------------------------
/src/lib/data.ts:
--------------------------------------------------------------------------------
  1 | import { colors } from "./colors";
  2 | 
  3 | export interface Playlist {
  4 |   id: string;
  5 |   title: string;
  6 |   color: (typeof colors)[keyof typeof colors];
  7 |   cover: string;
  8 |   artists: string[];
  9 | }
 10 | 
 11 | export const playlists: Playlist[] = [
 12 |   {
 13 |     id: "1",
 14 |     title: "Electronic Party",
 15 |     color: colors.teal,
 16 |     cover:
 17 |       "https://res.cloudinary.com/dp3ppkxo5/image/upload/v1693776174/spotify-astro/playlist_1_yci5uf.jpg",
 18 |     artists: ["Avicii", "Alok"],
 19 |   },
 20 |   {
 21 |     id: "2",
 22 |     title: "Trance",
 23 |     color: colors.green,
 24 |     cover:
 25 |       "https://res.cloudinary.com/dp3ppkxo5/image/upload/v1693776174/spotify-astro/playlist_2_f9ymlx.jpg",
 26 |     artists: ["Tiesto", "Armin Van Buuren"],
 27 |   },
 28 |   {
 29 |     id: "3",
 30 |     title: "Trap Vibes",
 31 |     color: colors.rose,
 32 |     cover:
 33 |       "https://res.cloudinary.com/dp3ppkxo5/image/upload/v1693776175/spotify-astro/playlist_3_grshca.jpg",
 34 |     artists: ["Post Malone", "Travis Scott", "21 savage"],
 35 |   },
 36 |   {
 37 |     id: "4",
 38 |     title: "Beatles Classics",
 39 |     color: colors.red,
 40 |     cover:
 41 |       "https://res.cloudinary.com/dp3ppkxo5/image/upload/v1693776175/spotify-astro/playlist_4_ap5xnb.jpg",
 42 |     artists: ["The Beatles"],
 43 |   },
 44 |   {
 45 |     id: "5",
 46 |     title: "Electronic Dance",
 47 |     color: colors.pink,
 48 |     cover:
 49 |       "https://res.cloudinary.com/dp3ppkxo5/image/upload/v1693776175/spotify-astro/playlist_5_erjyb7.jpg",
 50 |     artists: ["Deadmau5"],
 51 |   },
 52 |   {
 53 |     id: "6",
 54 |     title: "Cow songs",
 55 |     color: colors.gray,
 56 |     cover:
 57 |       "https://res.cloudinary.com/dp3ppkxo5/image/upload/v1693776474/spotify-astro/R-15112137-1586815179-1911_fsyl58.jpg",
 58 |     artists: ["Saint Hilda", "Canada Buffalo"],
 59 |   },
 60 | ];
 61 | 
 62 | export const morePlaylists = [
 63 |   ...playlists.map((item) => ({
 64 |     ...item,
 65 |     id: item.id + "a",
 66 |   })),
 67 | ];
 68 | 
 69 | export const sidebarPlaylists = [
 70 |   ...playlists.map((item) => ({
 71 |     ...item,
 72 |     id: item.id + "_side",
 73 |   })),
 74 | ];
 75 | 
 76 | export const allPlaylists = [
 77 |   ...playlists,
 78 |   ...morePlaylists,
 79 |   ...sidebarPlaylists,
 80 | ];
 81 | 
 82 | interface Song {
 83 |   id: string;
 84 |   title: string;
 85 |   image: string;
 86 |   artists: string[];
 87 |   album: string;
 88 |   duration: string;
 89 | }
 90 | const songScale = "w_40,h_40,c_scale";
 91 | export const songs: Song[] = [
 92 |   {
 93 |     id: "1",
 94 |     title: "The Nights",
 95 |     image: `https://res.cloudinary.com/dp3ppkxo5/image/upload/${songScale}/v1693776175/spotify-astro/song_1_qitfwl.jpg`,
 96 |     artists: ["Avicii"],
 97 |     album: "The Days / Nights",
 98 |     duration: "2:56",
 99 |   },
100 |   {
101 |     id: "2",
102 |     title: "Saint-Tropez",
103 |     image: `https://res.cloudinary.com/dp3ppkxo5/image/upload/${songScale}/v1693776175/spotify-astro/song_2_cijs8v.jpg`,
104 |     artists: ["Post Malone"],
105 |     album: "Hollywood's Bleeding",
106 |     duration: "2:23",
107 |   },
108 |   {
109 |     id: "3",
110 |     title: "SICKO MODE",
111 |     image: `https://res.cloudinary.com/dp3ppkxo5/image/upload/${songScale}/v1693776176/spotify-astro/song_3_td9ncs.jpg`,
112 |     artists: ["Travis Scott", "Drake"],
113 |     album: "ASTROWORLD",
114 |     duration: "5:13",
115 |   },
116 |   {
117 |     id: "4",
118 |     title: "Blinding Lights",
119 |     image: `https://res.cloudinary.com/dp3ppkxo5/image/upload/${songScale}/v1693776176/spotify-astro/song_4_lwumgu.png`,
120 |     artists: ["The Weeknd"],
121 |     album: "After Hours",
122 |     duration: "3:22",
123 |   },
124 |   {
125 |     id: "5",
126 |     title: "Shape of You",
127 |     image: `https://res.cloudinary.com/dp3ppkxo5/image/upload/${songScale}/v1693776175/spotify-astro/song_5_rd5xqa.jpg`,
128 |     artists: ["Ed Sheeran"],
129 |     album: "÷ (Divide)",
130 |     duration: "3:53",
131 |   },
132 |   {
133 |     id: "6",
134 |     title: "Uptown Funk",
135 |     image: `https://res.cloudinary.com/dp3ppkxo5/image/upload/${songScale}/v1693776175/spotify-astro/song_6_f1lt7y.jpg`,
136 |     artists: ["Mark Ronson", "Bruno Mars"],
137 |     album: "Uptown Special",
138 |     duration: "4:30",
139 |   },
140 |   {
141 |     id: "7",
142 |     title: "Bad Guy",
143 |     image: `https://res.cloudinary.com/dp3ppkxo5/image/upload/${songScale}/v1693776175/spotify-astro/song_7_m7f0mh.jpg`,
144 |     artists: ["Billie Eilish"],
145 |     album: "When We All Fall Asleep, Where Do We Go?",
146 |     duration: "3:14",
147 |   },
148 |   {
149 |     id: "8",
150 |     title: "Yesterday",
151 |     image: `https://res.cloudinary.com/dp3ppkxo5/image/upload/${songScale}/v1693776175/spotify-astro/song_8_hwxisr.jpg`,
152 |     artists: ["The Beatles"],
153 |     album: "Today & Tomorrow",
154 |     duration: "4:38",
155 |   },
156 |   {
157 |     id: "9",
158 |     title: "Havana",
159 |     image: `https://res.cloudinary.com/dp3ppkxo5/image/upload/${songScale}/v1693776176/spotify-astro/song_9_szemzp.jpg`,
160 |     artists: ["Camila Cabello", "Young Thug"],
161 |     album: "Camila",
162 |     duration: "3:37",
163 |   },
164 |   {
165 |     id: "10",
166 |     title: "Radioactive",
167 |     image: `https://res.cloudinary.com/dp3ppkxo5/image/upload/${songScale}/v1693776176/spotify-astro/song_10_sz0cib.jpg`,
168 |     artists: ["Imagine Dragons"],
169 |     album: "Night Visions",
170 |     duration: "3:07",
171 |   },
172 | ];
173 | 


--------------------------------------------------------------------------------
/src/pages/index.astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | import GreetingTitle from "../components/GreetingTitle.svelte";
 3 | import PageHeader from "../components/PageHeader.astro";
 4 | import PlaylistCard from "../components/PlaylistCard.astro";
 5 | import PlaylistItemCard from "../components/PlaylistItemCard.astro";
 6 | import Layout from "../layouts/Layout.astro";
 7 | import { playlists, morePlaylists } from "../lib/data";
 8 | ---
 9 | 
10 | <Layout title="Home">
11 |   <div
12 |     id="playlist-container"
13 |     class="relative transition-all duration-1000 bg-context"
14 |     style="min-height:300px;--context-color:#134e4a;"
15 |   >
16 |     <PageHeader />
17 |     <div class="relative z-10 px-6">
18 |       <GreetingTitle client:visible />
19 |       <div
20 |         class="grid gap-y-4 gap-x-6 sm:grid-cols-2 lg:grid-cols-2 xl:grid-cols-3 mt-6"
21 |       >
22 |         {playlists.map((playlist) => <PlaylistItemCard playlist={playlist} />)}
23 |       </div>
24 |     </div>
25 |     <div
26 |       class="absolute inset-0 bg-gradient-to-t from-zinc-900 via-zinc-900/80"
27 |     >
28 |     </div>
29 |   </div>
30 |   <div class="px-6 relative z-10 mt-4">
31 |     <h2 class="text-2xl font-bold">Made for you</h2>
32 |     <div class="flex flex-wrap mt-6 gap-4">
33 |       {morePlaylists.map((playlist) => <PlaylistCard playlist={playlist} />)}
34 |     </div>
35 |   </div>
36 | </Layout>
37 | 


--------------------------------------------------------------------------------
/src/pages/playlist/[id].astro:
--------------------------------------------------------------------------------
 1 | ---
 2 | const { id } = Astro.params;
 3 | import DotsButton from "../../components/DotsButton.astro";
 4 | import InlineArtists from "../../components/InlineArtists.astro";
 5 | import LikeButton from "../../components/LikeButton.astro";
 6 | import MusicsTable from "../../components/MusicsTable.astro";
 7 | import PageHeader from "../../components/PageHeader.astro";
 8 | import PlayButton from "../../components/PlayButton.astro";
 9 | import Layout from "../../layouts/Layout.astro";
10 | import { allPlaylists } from "../../lib/data";
11 | 
12 | export function getStaticPaths() {
13 |   return allPlaylists.map((playlist) => ({
14 |     params: {
15 |       id: playlist.id,
16 |     },
17 |   }));
18 | }
19 | 
20 | const playlist = allPlaylists.find((playlist) => playlist.id === id);
21 | ---
22 | 
23 | <Layout image={playlist?.cover} title={playlist?.title || "404"}>
24 |   <div
25 |     class="relative bg-zinc-900 min-h-full flex flex-col overflow-x-hidden rounded-lg"
26 |     transition:name=`playlist ${playlist?.id} box`
27 |   >
28 |     <PageHeader />
29 |     <div
30 |       class="flex flex-col items-center md:flex-row md:items-stretch gap-8 px-6"
31 |     >
32 |       <div class="h-52 w-52 flex-none">
33 |         <img
34 |           src={playlist?.cover}
35 |           alt={playlist?.title}
36 |           class="object-cover h-full w-full shadow-[5px_0_30px_0px_rgba(0,0,0,0.3)]"
37 |           transition:name=`playlist ${playlist?.id} image`
38 |         />
39 |       </div>
40 |       <div class="flex flex-col justify-between">
41 |         <div class="flex flex-1 items-end">Playlist</div>
42 |         <div>
43 |           <h1 class="title-clamp font-bold block">
44 |             {playlist?.title}
45 |             <span transition:name=`playlist ${playlist?.id} title`></span>
46 |           </h1>
47 |         </div>
48 |         <div class="flex-1 flex items-end">
49 |           <div class="text-sm">
50 |             <InlineArtists artists={playlist?.artists || []} />
51 |             <div class="mt-1">
52 |               <span class="font-semibold">58 likes</span>, 83 musics, <span
53 |                 class="text-gray-300">about 3h 15min</span
54 |               >
55 |             </div>
56 |           </div>
57 |         </div>
58 |       </div>
59 |     </div>
60 | 
61 |     <div class="bg-zinc-900/30 mt-6 flex-1 p-6 blur-100">
62 |       <div class="flex gap-1 items-center">
63 |         <PlayButton size="lg" />
64 |         <div class="ml-4" transition:name=`playlist ${playlist?.id} play`></div>
65 |         <LikeButton />
66 |         <DotsButton />
67 |       </div>
68 |       <div class="px-6 pt-4">
69 |         <MusicsTable />
70 |       </div>
71 |     </div>
72 |     <div
73 |       class="absolute h-screen inset-0 z-[-1] bg-gradient-to-b from-context"
74 |       style=`--context-color:${playlist?.color.accent}`
75 |     >
76 |       <img
77 |         src={playlist?.cover}
78 |         alt={playlist?.title}
79 |         class="el-to-fade transition-all duration-500 z-[-1] absolute inset-0 mix-blend-overlay opacity-20 scale-90 w-full h-full object-cover blur-md"
80 |       />
81 |       <div
82 |         class="absolute inset-0 bg-gradient-to-t via-transparent from-zinc-900"
83 |       >
84 |       </div>
85 |     </div>
86 |   </div>
87 | </Layout>
88 | 
89 | <style>
90 |   .title-clamp {
91 |     font-size: clamp(20px, 6vw, 70px);
92 |     line-height: 1;
93 |   }
94 | </style>
95 | 


--------------------------------------------------------------------------------
/svelte.config.js:
--------------------------------------------------------------------------------
1 | import { vitePreprocess } from '@astrojs/svelte';
2 | 
3 | export default {
4 | 	preprocess: vitePreprocess(),
5 | };
6 | 


--------------------------------------------------------------------------------
/tailwind.config.cjs:
--------------------------------------------------------------------------------
 1 | /** @type {import('tailwindcss').Config} */
 2 | module.exports = {
 3 |   content: ["./src/**/*.{astro,html,js,jsx,md,mdx,svelte,ts,tsx,vue}"],
 4 |   theme: {
 5 |     extend: {
 6 |       colors: {
 7 |         context: "var(--context-color)",
 8 |       },
 9 |     },
10 |   },
11 |   darkMode: "class",
12 |   plugins: [],
13 | };
14 | 


--------------------------------------------------------------------------------
/tsconfig.json:
--------------------------------------------------------------------------------
1 | {
2 |   "extends": "astro/tsconfigs/strict"
3 | }


--------------------------------------------------------------------------------
 Add to README

Other Tools
API

