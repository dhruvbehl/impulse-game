# impulse-game
Impulse is a game to check your reaction time by clicking on the appearing shapes on the screen. It is an effort to understand and implement protobuf, grpc &amp; rest framework gin using golang.

# Game Components
The game consists of 5 major services:
1. **[game-apis](https://github.com/dhruvbehl/game-apis)**: This is the model that the game gRPC server & clients use to interact with other services. This contains a protobuf resources which are compiled to autogenerate game-api code using the prooc tool.
2. **[game-highscore](https://github.com/dhruvbehl/game-highscore): This is a gRPC service that maintains the highscore of a game session and also provides getter and setter funcionalities for the same
3. **[game-engine]**(https://github.com/dhruvbehl/game-engine): This is a gRPC server that is the logic backbone of the game, here the base logic of deciding the difficulty of the game based on the user's performace is decided
4. **[game-mgmtplane]**(https://github.com/dhruvbehl/game-mgmtplane): This is a proxy service that converts rest call made by the frontend to gRPC and routes it to the appropriate gRPC service.
5. **[game-fontend]**(https://github.com/dhruvbehl/game-frontend): This contains a basic HTML, CSS, JS resource to provide a frontend to the game.

## Game architecture

<img width="797" alt="Screen Shot 2022-02-14 at 3 31 20 PM" src="https://user-images.githubusercontent.com/3843254/153842513-d5fcf4ea-63c0-4ebc-9e86-1b0168a15b56.png">


## Reference
1. https://grpc.io/docs/what-is-grpc/introduction/
2. https://grpc.io/docs/languages/go/quickstart/
3. https://github.com/gin-gonic/gin
4. https://www.justforlearning.com
