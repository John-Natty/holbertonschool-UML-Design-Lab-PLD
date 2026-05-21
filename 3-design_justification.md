# Design Justification

## Main Design Decisions

For this project, I chose the **Music Streaming Platform** scenario.

The system is based on five main classes:

- `User`
- `Playlist`
- `Song`
- `Album`
- `Artist`

These classes were chosen because they represent the main entities described in the scenario.

The design follows the music structure:

```text
Artist -> Album -> Song
```

and the user interaction structure:

```text
User -> Playlist -> Song
User -> Artist
```

I kept the model simple and avoided extra features such as playback, subscriptions, recommendations, or payments because they are not required.

## Responsibility Distribution

Each class has a clear responsibility.

`User` represents the person using the platform. It can create playlists, add songs, remove songs, and follow artists.

`Playlist` manages a collection of songs. It can add, remove, and return songs.

`Song` represents a music track. It belongs to one album and can appear in many playlists.

`Album` groups songs together and belongs to one artist.

`Artist` represents the creator of albums and can be followed by users.

## Relationships and Multiplicities

A `User` can create zero or many `Playlist` objects, but each playlist belongs to one user.

A `User` can follow many `Artist` objects, and an artist can be followed by many users.

A `Playlist` can contain many `Song` objects, and a song can appear in many playlists.

An `Artist` can create zero or many `Album` objects, but each album belongs to one artist.

An `Album` contains one or many `Song` objects, and each song belongs to one album.

## Alternatives Considered

I considered adding a `Library` class, but it was not necessary for the selected use cases.

I also considered adding playback-related classes, but the scenario specifically says to avoid modeling streaming or playback behavior.

## Trade-offs

This design is simple, clear, and focused on the required use cases.

The main advantage is that it is easy to understand and justify.

The limitation is that it does not include advanced features like user libraries, recommendations, subscriptions, or music playback.

## Conclusion

This design supports the selected use cases while staying consistent with the project requirements.

It focuses on playlist management, music organization, and the relationship between users and artists.