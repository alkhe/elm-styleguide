# elm-styleguide

Beginner Template

```elm
import Html exposing (..)
import Html.App exposing (beginnerProgram)
import Html.Events exposing (..)

main = beginnerProgram { model = null, update = update, view = view }

type alias Model = {
  content : String
}

type Msg = Content String

null : Model
null = { content = "" }

update : Msg -> Model -> Model
update msg model =
  case msg of
    Content s -> { model | content = s }

view : Model -> Html Msg
view { content } = div [] [
  input [onInput Content] [],
  text content
  ]
```
