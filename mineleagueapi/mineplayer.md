# MinePlayer

```bash
MinePlayer minePlayer = MineLeagueAPI.getInstance().getMinePlayer(UUID uuid);

minePlayer.getCoins();
minePlayer.addCoins(int coins);
minePlayer.removeCoins(int coins);
minePlayer.setCoins(int coins);


Playtime playtime = minePlayer.getPlaytime();
playtime.getHours();
playtime.getMinutes();
playtime.getSeconds();


Language language = minePlayer.getLanguage();
language.getLanguageId();
language.getMessages(); # the method getMessages get the registered messages for the selected language
```

