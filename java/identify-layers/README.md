# Identify Layers

This sample demonstrates how to identify features on a map across different layers present in the map.

![Identify Layers App](identify-layers.png)

## How to use the sample

Tap on map to get features at that location. The features are returned from different layers in the map.

## Features

* ArcGISMapImageLayer
* FeatureLayer
* FeatureTable
* MapView

## How it works

`MapView` has a `identifyLayersAsync(screenLocation, tolerance, returnPopupsOnly, maximumResults)` method that is used in the sample. The method takes a screen location, tolerance, boolean for returning (a pop-up/pop-up and geo-element), and maximum results per layer, which results in a `ListenableFuture<List<IdentifyLayerResult>>`.
	
Layer name and a count of identified features held by each `IdentifyLayerResult` in the `ListenableFuture<List<...>>` is then taken and written out to a String. Finally, the resulting String is displayed in an Android AlertDialog.