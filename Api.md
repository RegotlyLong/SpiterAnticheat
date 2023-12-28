# Spiter APIs

This is the document of API references of Spiter Anti-Cheat system.
Feel free to contact if theres any further questions.

------------

#### SpiterFlagEvent
Calls when: **A player was just flagged.**
Parameters:
- getPlayer(): **Get the player that has been flagged**
- getCheck(): **Gets the check associated with the flag.**
- getType(): **Gets the type of check.**
- getInfo(): **Gets additional information about the check if specified check description persists, otherwise gets the source of flag. (spiter, alerts, forceban)**
- getVl(): **Gets current violation of the player when they were flagged.**
- getMaxvl(): **Gets the maximum violation level for the check.**
- getTimestamp(): **Gets the time when the flag occurred in milliseconds unit.**

**Example:**

```java
    /**
     * Calls when a player was flagged.
     *
     * @param event The {@link me.regotlys.spiter.api.SpiterFlagEvent} to be processed.
     */
    @EventHandler(priority = EventPriority.MONITOR, ignoreCancelled = true)
    public void onPlayerFlag(SpiterFlagEvent event) {
        flag(event.getPlayer(), event.getCheck(), event.getType(), event.getInfo(), event.getVl(), event.getMaxvl(), event.getTimestamp());
    }

    /**
     * Logic to run when a player was flagged.
     *
     * @param player     The player to be flagged.
     * @param check      The check associated with the flag (e.g. Timer).
     * @param type       The type of check (e.g. 'A').
     * @param info       Additional information about the flag.
     * @param vl         The violation level.
     * @param maxVL      The maximum violation level.
     * @param timestamp  The timestamp of the flag, in milliseconds unit.
     */
    public void flag(Player player,
                     String check, String type, String info,
                     int vl, int maxVL, long timestamp) {
        // Implement method...
    }
```

------------

#### SpiterGhostBlockEvent
Calls when: **A player has encountered ghost blocks.**

**Example**

```java
    /**
     * Calls when a player encountered ghost blocks.
     *
     * @param event The {@link me.regotlys.spiter.api.SpiterGhostBlockEvent} to be processed.
     */
    @EventHandler(priority = EventPriority.MONITOR)
    public void onGhostBlock(SpiterGhostBlockEvent event) {
        // Implement method...
    }
```
