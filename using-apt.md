# using apt

`apt list --upgradable`
`apt update`
`apt upgrade`
`apt install <package_name>`: Installs a specific package.
`apt remove <package_name>`: Removes a package but keeps configuration files.
`apt purge <package_name>`: Removes a package and all its configuration files.
`apt install -f`: Attempts to fix broken dependencies during installation.
`apt show <package_name>`: Shows detailed information about a package.
`apt depends <package_name>`: Lists the dependencies of a package.
`apt search <keyword>`: Searches for packages based on keywords.
`apt full-upgrade`: Upgrades packages and also removes any outdated packages.
`apt autoremove`: Removes unused dependencies automatically.
`apt clean`: Removes all downloaded package files (.deb).
`apt autoclean`: Removes only outdated downloaded package files, keeping the latest ones.
`apt edit-sources`: Opens the sources.list file for editing repository configurations.
`apt-cache policy <package_name>`: Shows the installation state and available versions of a package.
`apt-cache show <package_name>`: Shows detailed information about a package from the cache.
`apt-get install <package_name>`: Installs a specific package.
`apt-get install -f`: Attempts to fix broken dependencies during installation.
`apt-get install -d <package_name>`: Downloads the package without installing it.
`apt-get remove <package_name>`: Removes a package but keeps configuration files.
`apt-get purge <package_name>`: Removes a package and all its configuration files.
`apt-get upgrad`e: Upgrades all installed packages to the latest versions.
`apt-get dist-upgrade`: Upgrades packages and also removes any outdated packages.
`apt-get show <package_name>`: Shows detailed information about a package.
`apt-get depends <package_name>`: Lists the dependencies of a package.
`apt-get search <keyword>`: Searches for packages based on keywords.
`apt-get update`: Updates the package list with the latest information from repositories.
`apt-get autoremove`: Removes unused dependencies automatically.
`apt-get clean`: Removes all downloaded package files (.deb).
`apt-get autoclean`: Removes only outdated downloaded package files, keeping the latest ones.