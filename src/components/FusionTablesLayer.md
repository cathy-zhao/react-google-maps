## Usage

```jsx static
import { compose, withProps } from "recompose";
import {
  withGoogleMap,
  GoogleMap,
  FusionTablesLayer,
} from "react-google-maps";
import withScriptjs from "react-google-maps/lib/async/withScriptjs";

const MapWithAFusionTablesLayer = compose(
  withProps({
    googleMapURL: "https://maps.googleapis.com/maps/api/js?v=3.exp",
    loadingElement: <div style={{ height: `100%` }} />,
    containerElement: <div style={{ height: `600px` }} />,
    mapElement: <div style={{ height: `100%` }} />,
  }),
  withScriptjs,
  withGoogleMap
)(props =>
  <GoogleMap
    defaultZoom={11}
    defaultCenter={{ lat: 41.850033, lng: -87.6500523 }}
  >
    <FusionTablesLayer
      url="http://googlemaps.github.io/js-v2-samples/ggeoxml/cta.kml"
      options={{
        query: {
          select: `Geocodable address`,
          from: `1mZ53Z70NsChnBMm-qEYmSDOvLXgrreLTkQUvvg`
        }
      }}
    />
  </GoogleMap>
);

<MapWithAFusionTablesLayer />
```

### Map with a FusionTablesLayer

```jsx
const { compose, withProps } = require("recompose");
const {
  withGoogleMap,
  GoogleMap,
  FusionTablesLayer,
} = require("../index");
const { default: withScriptjs } = require("../async/withScriptjs");

const MapWithAFusionTablesLayer = compose(
  withProps({
    googleMapURL: "https://maps.googleapis.com/maps/api/js?v=3.exp",
    loadingElement: <div style={{ height: `100%` }} />,
    containerElement: <div style={{ height: `600px` }} />,
    mapElement: <div style={{ height: `100%` }} />,
  }),
  withScriptjs,
  withGoogleMap
)(props =>
  <GoogleMap
    defaultZoom={11}
    defaultCenter={{ lat: 41.850033, lng: -87.6500523 }}
  >
    <FusionTablesLayer
      url="http://googlemaps.github.io/js-v2-samples/ggeoxml/cta.kml"
      options={{
        query: {
          select: `Geocodable address`,
          from: `1mZ53Z70NsChnBMm-qEYmSDOvLXgrreLTkQUvvg`
        }
      }}
    />
  </GoogleMap>
);

<MapWithAFusionTablesLayer />
```
