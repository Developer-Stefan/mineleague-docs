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

## Examples

```bash
@EventHandler
    public void handlePlayerJoin(PlayerJoinEvent event) {
        Player player = event.getPlayer();
        MinePlayer minePlayer = MineLeagueAPI.getInstance().getMinePlayer(player.getUniqueId());
        Playtime playtime = minePlayer.getPlaytime();
        Language language = minePlayer.getLanguage();
        Map<String, String> messages = language.getMessages();

        // In the onEnable Section: Register some Messages for DE & EN
        // Send some information to the player
        int hours = playtime.getHours();
        int minutes = playtime.getMinutes();
        int seconds = playtime.getSeconds();
        player.sendMessage(messages.get("this.is.an.example.path").replaceAll("%time%", hours + ":" + minutes + ":" + seconds));

        int currentCoins = minePlayer.getCoins();
        player.sendMessage(messages.get("player.see.current.coins").replaceAll("%coins%", String.valueOf(currentCoins)));
        // Change the coins of the player
        minePlayer.addCoins(1000);
        minePlayer.removeCoins(1000);
        minePlayer.setCoins(1000);
}
```

