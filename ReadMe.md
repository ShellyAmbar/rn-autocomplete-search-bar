- A react native auto complete search bar, in typescript.

- It comes with a built-in TypeScript typings and is compatible with all popular JavaScript frameworks. You can use it directly or leverage well-maintained wrapper packages that allow for a more native integration with your frameworks of choice.

# Example:

![](./assets/videos/1.gif)

## How to use:

```
import SearchBar from 'rn-autocomplete-search-bar';

   <SearchBar
          isAutoCompleteSearch={false}
          onSelectResult={(resultItem) => {
            console.log(resultItem);
            setIsShowPlaces(true);
          }}
          onClickSearch={(search) => {
            console.log(search);

            setIsShowPlaces(true);
          }}
          onPressDelete={() => {}}
          textInputStyle={{color: "#FFFF"}}
          onFocus={() => {
            setIsShowPlaces(false);
          }}
          onSubmitEditing={() => {
            setIsShowPlaces(true);
          }}
          searchbarContainerStyle={{
            backgroundColor: "rgba(255,255,255,0.3)",
          }}
          icon={() => <Search width={20} height={20} />}
          data={[
            {id: "0", name: "bara 1"},
            {id: "1", name: "barb 2"},
            {id: "2", name: "barab 3"},
            {id: "3", name: "barabc 4"},
            {id: "4", name: "barrca 5"},
            {id: "5", name: "barar 6"},
          ]}
        />
```

# Props -

| Name                     | Type                               |
| ------------------------ | ---------------------------------- |
| viewContainerStyle       | ? ViewStyle                        |
| searchbarContainerStyle  | ? ViewStyle                        |
| buttonSearchStyle        | ? ViewStyle                        |
| cancleButtonStyle        | ? ViewStyle                        |
| textInputStyle           | ? TextStyle;                       |
| onSelectResult           | ? (searchItem: SearchItem) => void |
| onClickSearch            | ? (searchTerm: string) => void     |
| onPressDelete            | ? () => void                       |
| data                     | ? SearchItem[]                     |
| resultsContainerStyle    | ? ViewStyle                        |
| resultItemContainerStyle | ? ViewStyle                        |
| resultItemTextStyle      | ? ViewStyle                        |
| isAutoCompleteSearch     | ? boolean                          |
| icon                     | ? () => any                        |
