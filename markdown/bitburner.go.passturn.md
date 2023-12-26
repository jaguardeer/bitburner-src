<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [bitburner](./bitburner.md) &gt; [Go](./bitburner.go.md) &gt; [passTurn](./bitburner.go.passturn.md)

## Go.passTurn() method

Pass the player's turn rather than making a move, and await the opponent's response. This ends the game if the opponent passed on the previous turn, or if the opponent passes on their following turn.

This can also be used if you pick up the game in a state where the opponent needs to play next. For example: if BitBurner was closed while waiting for the opponent to make a move, you may need to call passTurn() to get them to play their move on game start.

**Signature:**

```typescript
passTurn(): Promise<{
    type: "invalid" | "move" | "pass" | "gameOver";
    x: number;
    y: number;
    success: boolean;
  }>;
```
**Returns:**

Promise&lt;{ type: "invalid" \| "move" \| "pass" \| "gameOver"; x: number; y: number; success: boolean; }&gt;

a promise that contains if your move was valid and successful, the opponent move's x and y coordinates (or pass) in response, or an indication if the game has ended

## Remarks

RAM cost: 0 GB
