# tflite models

use them for testing - drop them in the assets folder of the rn application, or change the urls to point to the raw files from this repo

# sao

optimized for ARM

# adding conditioners with int32 input


shasum -a 256 sao/*.tflite

Get-FileHash -Algorithm SHA256 .\sao\*.tflite | ForEach-Object { "{0}  {1}" -f $_.Hash.ToLower(), (Split-Path $_.Path -Leaf) }
