1- main entities

- User (la personne qui utilise la plateforme )
- Playlist ( les utilisateur doivent pouvoir créer leurs propres playlists)
- Song ( l'élément musical principal que User manipule)
- Album ( il sert a organiser les chansons )
- Artist ( un Album doit être fait par l'Artiste et l'User doit pouvoir le follow )

2- Key  relationships

`Artist 1->0..* Album`
( un Artist doit pouvoir créer un ou plusieurs album)

`Album 1->1..* Song`
( un Album doit pouvoir contenir une ou plusieurs Song)

`Song 1->1 Album`
( un Song doit obligatoirement appartenir a un Album)

`User 1->0..* Playlist`
( un User peut créer une ou plusieurs Playlist)

`Playlist 0..*->0..* Song`
( une ou plusieurs Playlist peut contenir plusieurs Song)

`User 0..*->0..* Artist`
( un ou plusieurs User peut suivre un ou plusieurs Artist)

3- Main actions / use cases

- Add a song to a playlist 
( l'élément principal et obligatoire)

additional: 
- Create a playlist
                ( avant d'ajouter une chanson a une playlist il faut pouvoir la créer)
- Remove a song from a playlist
                ( pouvoir gérer ça playlist et supprimer des Song )