<h2> gh-action-deploy-cf </h2>

This GitHub Action will deploy `SAP CAP project` to Cloud Foundry (`cf`)

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Usage](#usage)
  - [Parameters](#parameters)
  - [Example](#example)
- [Contributing](#contributing)
- [License](#license)
- [Authors](#authors)

## Usage

### Parameters

| Parameter          | Description                                                                                  |
| ------------------ | -------------------------------------------------------------------------------------------- |
| `CF_IAS_ORIGIN`    | The origin to be used for IAS authentication when logging into Cloud Foundry.                |
| `CF_API_DEV`       | The API endpoint for the development Cloud Foundry environment.                              |
| `CF_ORG_DEV`       | The organization for the development environment in Cloud Foundry.                           |
| `CF_SPACE_DEV`     | The space within the development organization in Cloud Foundry.                              |
| `CF_USERNAME_DEV`  | The username for logging into the development environment in Cloud Foundry.                  |
| `CF_PASSWORD_DEV`  | The password for logging into the development environment in Cloud Foundry.                  |
| `CF_API_PROD`      | The API endpoint for the production Cloud Foundry environment.                               |
| `CF_ORG_PROD`      | The organization for the production environment in Cloud Foundry.                            |
| `CF_SPACE_PROD`    | The space within the production organization in Cloud Foundry.                               |
| `CF_USERNAME_PROD` | The username for logging into the production environment in Cloud Foundry.                   |
| `CF_PASSWORD_PROD` | The password for logging into the production environment in Cloud Foundry.                   |
| `CF_API_QA`        | (Optional) The API endpoint for the QA Cloud Foundry environment, if applicable.             |
| `CF_ORG_QA`        | (Optional) The organization for the QA environment in Cloud Foundry, if applicable.          |
| `CF_SPACE_QA`      | (Optional) The space within the QA organization in Cloud Foundry, if applicable.             |
| `CF_USERNAME_QA`   | (Optional) The username for logging into the QA environment in Cloud Foundry, if applicable. |
| `CF_PASSWORD_QA`   | (Optional) The password for logging into the QA environment in Cloud Foundry, if applicable. |

<p align="right">(<a href="#table-of-contents">back to top</a>)</p>

### Example

Add the following as a job in your GitHub Actions workflow:

```yaml
- name: Bump version and create release
  uses: dxfrontier/gh-action-deploy-cf@main
  with:
    # Common
    CF_IAS_ORIGIN: ${{ secrets.CF_IAS_ORIGIN }}

    # Development
    CF_API_DEV: ${{ secrets.CF_API_DEV }}
    CF_ORG_DEV: ${{ secrets.CF_ORG_DEV }}
    CF_SPACE_DEV: ${{ secrets.CF_SPACE_DEV }}
    CF_USERNAME_DEV: ${{ secrets.CF_USERNAME_DEV }}
    CF_PASSWORD_DEV: ${{ secrets.CF_PASSWORD_DEV }}

    # Production
    CF_API_PROD: ${{ secrets.CF_API_PROD }}
    CF_ORG_PROD: ${{ secrets.CF_API_PROD }}
    CF_SPACE_PROD: ${{ secrets.CF_API_PROD }}
    CF_USERNAME_PROD: ${{ secrets.CF_USERNAME_PROD }}
    CF_PASSWORD_PROD: ${{ secrets.CF_PASSWORD_PROD }}
    # QA is optional, added if necessary ...
```

<p align="right">(<a href="#table-of-contents">back to top</a>)</p>

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

![Licence](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)

Copyright (c) 2024 DXFrontier

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Authors

- [@mathiasvkaiz](https://github.com/mathiasvkaiz)
- [@dragolea](https://github.com/dragolea)
- [@sblessing](https://github.com/sblessing)
- [@ABS GmbH](https://www.abs-gmbh.de/) team

<p align="right">(<a href="#table-of-contents">back to top</a>)</p>
