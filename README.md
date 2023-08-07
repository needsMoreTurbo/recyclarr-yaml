# recyclarr-yaml
Collection of YAML files for recyclarr based on https://trash-guides.info/

These files are created by processing the Trash Guide Documentation repo and are intended to simplify the process of keeping up to date with changes until there is facility to do this directly through recyclarr. The clones folders contains additional copies Quality Profiles to allow for setting of different parameters, for example "Minimum" and "Update until" scores so you can tweak the profile based on the content you may be looking for and avoid multiple upgrades.

## Installation
1) Install recyclarr (v5.0.1 or higher) using instructions on https://recyclarr.dev/wiki/
2) Configure a script to set environment variables for the URLs and API Keys referenced in the YAML files

## Usage
1) Run the customformats/all*.yml files first to update all custom formats
2) Run the quality profiles for sonarr or radarr yamls as required (you will need to create them in the respective app first)

There are 3 sets of files, working on the assumption that there are multiple instances. Recyclarr requires the instance to be unique, so I've created one for Default, 4k and a Seedbox (sb) instance.

## Notes
If you would like more of the standard TRaSH guide Quality Profiles added here, please raise an issue.

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
