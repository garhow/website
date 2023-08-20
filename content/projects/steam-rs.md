---
title: "Steam.rs"
description: "Safe Rust bindings for the Steam Web API"
keywords: ["rust", "steam", "api"]
repository: https://github.com/garhow/steam-rs
package: https://crates.io/crates/steam-rs
documentation: https://docs.rs/steam-rs/latest/steam_rs/
license: "MIT"
deprecated: false
date: 2023-08-10T16:14:33-05:00
draft: false
---

Steam.rs is a library for Rust that provides safe, convenient bindings for the Steam WebAPI. Here's an example:

{{< highlight rust>}}
use std::env;
use steam_rs::{Steam, SteamId};

#[tokio::main]
async fn main() {
    // Get the Steam API Key as an environment variable
    let steam_api_key = env::var("STEAM_API_KEY").expect("Missing an API key");

    // Initialize the Steam API client
    let steam = Steam::new(steam_api_key);

    // Request the recently played games of SteamID `76561197960434622`
    let steam_id = SteamId::new(76561197960434622);
    let recently_played_games = steam.get_recently_played_games(steam_id, None).await.unwrap();

    // Print the total count of the user's recently played games
    println!("{}", recently_played_games.total_count);
}
{{</highlight>}}