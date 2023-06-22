# recyclarr-yaml
Collection of YAML files for recyclarr based on https://trash-guides.info/

## Installation
1) Install recyclarr using instructions at from https://recyclarr.dev/wiki/
2) Configure a script to set environment variables for the URLs and API Keys referenced in the YAML files

## Usage
1) Run the customformats/all*.yml files first to update all custom formats
2) Run the quality profiles for sonarr or radarr yamls as required (you will need to create them in the respective app first)

## Notes
If you would like more of the standard TRaSH guide Quality Profiles added here, please raise an issue. The clones folders contain additional copies of the quality profile to allow for setting of different parameters, for example Miniumum and Update until scores to avoid multiple downloads.

## Example command lines
Your command files will need to set up the appropriate environment variables prior to calling recyclarr. Adjust the filenames according to your own system setup.

The required variables are: SONARRURL, SONARRAPI, RADARRURL, RADARRAPI

### Custom Formats
```
recyclarr sync sonarr -c \recyclarr-yaml\customformats\all-sonarr.yml
recyclarr sync radarr -c \recyclarr-yaml\customformats\all-radarr.yml
```

### Quality Profiles
```
recyclarr sync sonarr -c \recyclarr-yaml\qualityprofiles\sonarr\WEB-1080p.yml
recyclarr sync radarr -c \recyclarr-yaml\qualityprofiles\radarr\HD Bluray + WEB.yml
```
