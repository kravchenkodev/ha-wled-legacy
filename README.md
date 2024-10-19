[![SWUbanner](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/banner-direct-single.svg)](https://stand-with-ukraine.pp.ua/)

# WLED Legacy

This integration was added to mitigate the loss of the original WLED integration after the update to WLED 0.14.0. All credits for the integration goes to original developer of [WLED integration](https://github.com/home-assistant/core/tree/dev/homeassistant/components/wled) as it is literally just the same thing.

> [!CAUTION]
> You can only have one WLED integration in your HA instance. You either choose this or the original WLED integration.

## Installation
If you have original WLED integration installed, you will have to remove it. The reason for this is because original integration installs WLED dependency as a requirement and we need another version of WLED installed.

### Remove original WLED integration
1. Remove original WLED integration
2. Get access to your homeassistant docker container
    - For **Home Assistant OS** users:
        - Open **Terminal**
        - Run `docker exec -it homeassistant sh`
    - For **Docker** users:
        - Run `docker exec -it homeassistant sh`
3. Go to `/usr/local/lib/python3.12/site-packages/`
4. Delete `wled` folder
5. Restart Home Assistant

### Install WLED Legacy integration
1. Visit **HACS** → **Integrations** → **...** (in the top right) → **Custom repositories**
2. Click **Add**
3. Paste `https://github.com/kravchenkodev/ha-wled-legacy` into the **URL** field
4. Chose **Integration** as a **Category**
5. **WLED Legacy** will appear in the list of available integrations. Install it normally.
