create sequence hibernate_sequence start with 1 increment by 1;
create table game
(
    game_id           bigint    not null,
    created           timestamp not null,
    current_state     integer,
    updated           timestamp not null,
    current_player_id bigint,
    primary key (game_id)
);
create table game_player
(
    game_player_id bigint    not null,
    created        timestamp not null,
    game_id        bigint    not null,
    player_id      bigint    not null,
    primary key (game_player_id)
);
create table player
(
    player_id    bigint not null,
    display_name varchar(255),
    oauth_key    varchar(255),
    primary key (player_id)
);
alter table player
    add constraint UKhlekxg3s1qrcev9cmska0c0lw unique (oauth_key);
alter table game
    add constraint FK4de0v58935dtit7o35m9s98y6 foreign key (current_player_id) references player;
alter table game_player
    add constraint FK8so14tnd5mqdjqabugc0cycxu foreign key (game_id) references game;
alter table game_player
    add constraint FK7ntwi66eylpagi55pmm4i61l5 foreign key (player_id) references player
