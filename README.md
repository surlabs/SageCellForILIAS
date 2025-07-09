![SageCell](https://github.com/user-attachments/assets/552ecd94-3452-4659-abd7-287d9f5ff440)

# SageCell Page Component Plugin for ILIAS

Welcome to the official repository for the SageCell Page Component Plugin for ILIAS.
This Open Source ILIAS Plugin was initially created by the Innovation in Learning Institute of the Friedrich-Alexander University of Erlangen and is currently maintained by [SURLABS](https://www.surlabs.com).

## What is SageCell for ILIAS?

SageCell is a Page Component plugin that enhances ILIAS pages by allowing authors to include Sage content.

### Software Requirements

- This plugin requires [PHP](https://php.net) version 8.1+ to work properly on your ILIAS platform.
- This plugin requires [ILIAS](https://www.ilias.de/docu/goto.php?target=latest_7&client_id=docu) version 9.x.

### Installation Steps

1.  Create necessary subdirectories if they do not exist:
    ```bash
    mkdir -p Customizing/global/plugins/Services/COPage/PageComponent
    cd Customizing/global/plugins/Services/COPage/PageComponent
    ```
2.  Clone the repository into a directory named `PCSageCell`:
    ```bash
    git clone https://github.com/surlabs/SageCellForILIAS.git ./PCSageCell
    cd PCSageCell
    git checkout main
    ```
3.  After installation or updating the plugin, run the following commands in the ILIAS root folder:
    ```bash
    composer install --no-dev
    npm install
    php setup/setup.php update
    ```
    **Important:** Make sure your main `composer.json` and ILIAS `.gitignore` files do **not** exclude plugins. Also, do **not** use the `--no-plugins` flag during ILIAS setup.


4.  Go to the ILIAS Plugin Administration page (Administration -> Plugins).
5.  Find the "PCSageCell" plugin in the list, click "Actions", and select "Install".
6.  After installation, click Then click "Actions" again and select "Activate".
7.  Configure the plugin as needed (e.g., API keys) by clicking "Actions" and then "Configure".
8.  The plugin is now ready to be used on ILIAS pages.

## Branching

- **main** (or **trunk**): Main development branch.
- **iliasX** (e.g., ilias9): Stable release branches corresponding to ILIAS 9 version.
<!-- TODO: Confirm actual branching strategy for PCSageCell -->

## Uninstalling the Plugin

To uninstall the plugin:

1.  Go to ILIAS Plugin Administration, find "PCSageCell", click "Actions", and select "Deactivate".
2.  Then, click "Actions" again and select "Uninstall".
3.  Remove the plugin directory from your ILIAS installation:
    ```bash
    rm -rf Customizing/global/plugins/Services/COPage/PageComponent/PCSageCell
    ```
4.  Run the following commands in the ILIAS root folder:
    ```bash
    composer du
    php setup/setup.php update
    ```

## License

This plugin is licensed under GPLv3. See the LICENSE file for details.

---

**Authors:**

- Initially created by [Institut für Lern-Innovation](https://ili.fau.de), Germany.
- Maintained by [SURLABS](https://surlabs.com), Spain.