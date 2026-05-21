# Diagramme 1 : Add a song to a playlist
```
sequenceDiagram
    actor User
    participant Playlist
    participant Song

    User->>Playlist: addSong(song)
    Playlist->>Song: getAlbum()
    Song-->>Playlist: album
    Playlist-->>User: song added
```

# Diagramme 2 : Create a playlist
```
sequenceDiagram
    actor User

    User->>User: createPlaylist(name)
    create participant NewPlaylist as Playlist
    User->>NewPlaylist: initialize name and createdAt
    NewPlaylist-->>User: playlist created
```

# Diagramme 3 : Remove a song from a playlist
```
sequenceDiagram
    actor User
    participant Playlist

    User->>Playlist: removeSong(song)
    Playlist->>Playlist: check if song exists
    Playlist->>Playlist: remove song
    Playlist-->>User: song removed
```