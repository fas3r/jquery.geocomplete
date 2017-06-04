
<p align="center">
  <img src="./github/logo.png" width=100 height=100 />

  <h3 align="center">
    jQuery Geocomplete
  </h3>

  <p align="center">
    A simple plugin for completing address forms.
    <br>
    <a href="http://projects.trentmentink.com/jquery_geocomplete/"><strong>View Demo &raquo;</strong></a>
  </p>
</p>

<br>

## Table of contents

- [Quick start](#quick-start)
- [Documentation](#documentation)
- [Credits](#credits)
- [License](https://github.com/tmentink/jquery.geocomplete/blob/master/LICENSE)
- [Author](http://www.trentmentink.com)

## Quick Start

**Add dependencies**
- [jQuery](https://code.jquery.com/)
- [Google Maps JavaScript API with Places Library](https://developers.google.com/maps/documentation/javascript/places)

**Add jQuery Geocomplete**
- [jquery.gecomplete.min.js](https://raw.githubusercontent.com/tmentink/jquery.geocomplete/master/dist/jquery.geocomplete.min.js)
- [jquery.gecomplete.min.css](https://raw.githubusercontent.com/tmentink/jquery.geocomplete/master/dist/jquery.geocomplete.min.css)

Select an input and call .geocomplete() with the fields you'd like to fill.
```javascript
$("#myInput").geocomplete({
  fields: {
    txtStreetAddress: "street address",
    txtCity: "city",
    txtState: "short state",
    txtZipCode: "zip code"
  }
})
```

## Documentation
You can set the defaults at **$.fn.geocomplete.Defaults**

### Settings
| Setting | Type | Default | Description |
| ---  | --- | ---  | --- |
| **appendToParent** | boolean | true | Appends the autogenerated .pac-container to the selected input's parent. This fixes the [scrolling issue](https://stackoverflow.com/questions/40143131/google-maps-autocomplete-fix-to-the-input). |
| **bounds** | LatLngBounds | undefined | [Google's Documentation](https://developers.google.com/maps/documentation/javascript/reference#AutocompleteOptions) |
| **componentRestrictions** | object | undefined | [Google's Documentation](https://developers.google.com/maps/documentation/javascript/reference#AutocompleteOptions) |
| **fields** | object | {} | The fields you would like to fill based on the search results. The key is the field's id. The value is the desired <a href="#address-types">Address Type</a>. |
| **geolocate** | boolean | false | Sets the bounds based on the browser's location. |
| **strictBounds** | boolean | false | [Google's Documentation](https://developers.google.com/maps/documentation/javascript/reference#AutocompleteOptions) |
| **types** | Array\<string> | ["geocode"] | [Google's Documentation](https://developers.google.com/maps/documentation/javascript/reference#AutocompleteOptions) |

### Address Types
You can access the **short_name** value by addding "short" in front of the type. Otherwise it will return the **long_name** value.

| Type | [Google Equivalent](https://developers.google.com/maps/documentation/geocoding/intro#Types) |
| --- | --- |
| **city** | locality |
| **country** | country |
| **county** | administrative_area_level_2 |
| **formatted address** | formatted_address |
| **neighborhood** | neighborhood |
| **state** | administrative_area_level_1 |
| **street** | route |
| **street address** | street_number + route |
| **street number** | street_number |
| **zip code** | postal_code |
| **zip code suffix** | postal_code_suffix |

### Methods

All the following methods can be called using the syntax:
```javascript
$("#myInput").geocomplete("method name", arguments)
```

| Method | Arguments | Returns | Description |
| --- | --- | --- | --- |
| **clear fields** | none | $selector | clears all the fields. This is automatically called before filling fields. |
| **fill fields** | none | $selector | fills all the fields based on the last selected location. This is automatically called when a location is selected. |
| **get bounds** | none | LatLngBounds | [Google's Documentation](https://developers.google.com/maps/documentation/javascript/reference#Autocomplete) |
| **get place** | none | PlaceDetails | [Google's Documentation](https://developers.google.com/maps/documentation/javascript/reference#Autocomplete) |
| **set bounds** | LatLngBounds | $selector | [Google's Documentation](https://developers.google.com/maps/documentation/javascript/reference#Autocomplete) |
| **set component restrictions** | Object | $selector | [Google's Documentation](https://developers.google.com/maps/documentation/javascript/reference#Autocomplete) |
| **set options** | Object | $selector | [Google's Documentation](https://developers.google.com/maps/documentation/javascript/reference#Autocomplete) |
| **set types** | Array\<string> | $selector | [Google's Documentation](https://developers.google.com/maps/documentation/javascript/reference#Autocomplete) |

## Credits
* [The jQuery Team](https://jquery.org/team/) - for creating jQuery
* [Google](https://www.google.com/intl/en/about/) - for creating Google Maps

## License
Code released under the [MIT License](https://github.com/tmentink/jquery.geocomplete/blob/master/LICENSE)

## Author
#### [Trent Mentink](http://www.trentmentink.com)
