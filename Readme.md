<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->

<h3 align="center">Superset K8s with Ingress and OAUTH</h3>

  <p align="center">
    Project Description
    This project aims to configure the values file in order to incorporate ingress and Oauth into the helm chart of Kubernetes Superset
    <br />
    <a href="https://github.com/Justinljg/SupersetK8s/"><strong>Explore the docs »</strong></a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#working-tree">Working Tree</a></li>
      </ul>
    </li>
    <li><a href="#Configurations">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>

  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][https://example.com](https://upload.wikimedia.org/wikipedia/commons/0/0e/Superset_logo.svg))

`justinljg`, `SupersetK8s`,`Superset K8s with Ingress and OAUTH`, `This project aims to configure the values file in order to incorporate ingress and Oauth into the helm chart of Kubernetes Superset`

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With
Helm
![helm-icon-color](https://user-images.githubusercontent.com/108221154/211633332-44e4cf02-208d-4eda-82b6-ca0cae967d75.png)
Superset
![Superset_logo svg](https://user-images.githubusercontent.com/108221154/211633387-7bebf2f0-6dfd-4b32-a442-f61ccf991573.png)
GCP
![download (1)](https://user-images.githubusercontent.com/108221154/211633555-364bde4d-d2a1-4498-858e-a649ff2d9d81.png)
Kubernetes
![download (2)](https://user-images.githubusercontent.com/108221154/211633652-2beab043-7ccb-48bc-83ef-6bd800978d35.png)
Spark SQL
![download](https://user-images.githubusercontent.com/108221154/211633719-ce0c66d1-b35e-4776-80d6-9a7dc4f38d1a.jpeg)


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

Open Terminal.

Change the current working directory to the location where you want the cloned directory.

Type git clone, and then paste the URL you copied earlier.

$ git clone https://github.com/Justinljg/SupersetK8s

More specific instructions can be seen in https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository if needed.

### Prerequisites

Please refer to the https://helm.sh/docs/intro/install/ instructions to install helm.
A snippet of the usage of script to install helm is as shown below:
'''
$ curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
$ chmod 700 get_helm.sh
$ ./get_helm.sh
'''
Please sign up and get a mapbox api key from https://docs.mapbox.com/help/getting-started/access-tokens/. The geographical visualisations will not work if you do not include the mapbox api key into the my-values.yaml file later.

### Working Tree

The following is the working tree of this repository.
"
.
├── charts
│   ├── postgresql
│   │   ├── Chart.lock
│   │   ├── charts
│   │   │   └── common
│   │   │       ├── Chart.yaml
│   │   │       ├── README.md
│   │   │       ├── templates
│   │   │       │   ├── _affinities.tpl
│   │   │       │   ├── _capabilities.tpl
│   │   │       │   ├── _errors.tpl
│   │   │       │   ├── _images.tpl
│   │   │       │   ├── _ingress.tpl
│   │   │       │   ├── _labels.tpl
│   │   │       │   ├── _names.tpl
│   │   │       │   ├── _secrets.tpl
│   │   │       │   ├── _storage.tpl
│   │   │       │   ├── _tplvalues.tpl
│   │   │       │   ├── _utils.tpl
│   │   │       │   ├── validations
│   │   │       │   │   ├── _cassandra.tpl
│   │   │       │   │   ├── _mariadb.tpl
│   │   │       │   │   ├── _mongodb.tpl
│   │   │       │   │   ├── _postgresql.tpl
│   │   │       │   │   ├── _redis.tpl
│   │   │       │   │   └── _validations.tpl
│   │   │       │   └── _warnings.tpl
│   │   │       └── values.yaml
│   │   ├── Chart.yaml
│   │   ├── ci
│   │   │   ├── extended-config.yaml
│   │   │   ├── init-scripts.yaml
│   │   │   ├── metrics.yaml
│   │   │   ├── rbac.yaml
│   │   │   ├── replication.yaml
│   │   │   └── tls.yaml
│   │   ├── README.md
│   │   ├── templates
│   │   │   ├── extra-list.yaml
│   │   │   ├── _helpers.tpl
│   │   │   ├── networkpolicy-egress.yaml
│   │   │   ├── NOTES.txt
│   │   │   ├── primary
│   │   │   │   ├── configmap.yaml
│   │   │   │   ├── extended-configmap.yaml
│   │   │   │   ├── initialization-configmap.yaml
│   │   │   │   ├── metrics-configmap.yaml
│   │   │   │   ├── metrics-svc.yaml
│   │   │   │   ├── networkpolicy.yaml
│   │   │   │   ├── prometheusrule.yaml
│   │   │   │   ├── servicemonitor.yaml
│   │   │   │   ├── statefulset.yaml
│   │   │   │   ├── svc-headless.yaml
│   │   │   │   └── svc.yaml
│   │   │   ├── psp.yaml
│   │   │   ├── read
│   │   │   │   ├── networkpolicy.yaml
│   │   │   │   ├── statefulset.yaml
│   │   │   │   ├── svc-headless.yaml
│   │   │   │   └── svc.yaml
│   │   │   ├── rolebinding.yaml
│   │   │   ├── role.yaml
│   │   │   ├── secrets.yaml
│   │   │   ├── serviceaccount.yaml
│   │   │   └── tls-secrets.yaml
│   │   ├── values.schema.json
│   │   └── values.yaml
│   └── redis
│       ├── Chart.lock
│       ├── charts
│       │   └── common
│       │       ├── Chart.yaml
│       │       ├── README.md
│       │       ├── templates
│       │       │   ├── _affinities.tpl
│       │       │   ├── _capabilities.tpl
│       │       │   ├── _errors.tpl
│       │       │   ├── _images.tpl
│       │       │   ├── _ingress.tpl
│       │       │   ├── _labels.tpl
│       │       │   ├── _names.tpl
│       │       │   ├── _secrets.tpl
│       │       │   ├── _storage.tpl
│       │       │   ├── _tplvalues.tpl
│       │       │   ├── _utils.tpl
│       │       │   ├── validations
│       │       │   │   ├── _cassandra.tpl
│       │       │   │   ├── _mariadb.tpl
│       │       │   │   ├── _mongodb.tpl
│       │       │   │   ├── _postgresql.tpl
│       │       │   │   ├── _redis.tpl
│       │       │   │   └── _validations.tpl
│       │       │   └── _warnings.tpl
│       │       └── values.yaml
│       ├── Chart.yaml
│       ├── ci
│       │   ├── extra-flags-values.yaml
│       │   ├── sentinel-values.yaml
│       │   └── standalone-values.yaml
│       ├── img
│       │   ├── redis-cluster-topology.png
│       │   └── redis-topology.png
│       ├── README.md
│       ├── templates
│       │   ├── configmap.yaml
│       │   ├── extra-list.yaml
│       │   ├── headless-svc.yaml
│       │   ├── health-configmap.yaml
│       │   ├── _helpers.tpl
│       │   ├── master
│       │   │   ├── psp.yaml
│       │   │   ├── service.yaml
│       │   │   └── statefulset.yaml
│       │   ├── metrics-svc.yaml
│       │   ├── networkpolicy.yaml
│       │   ├── NOTES.txt
│       │   ├── pdb.yaml
│       │   ├── prometheusrule.yaml
│       │   ├── replicas
│       │   │   ├── hpa.yaml
│       │   │   ├── service.yaml
│       │   │   └── statefulset.yaml
│       │   ├── rolebinding.yaml
│       │   ├── role.yaml
│       │   ├── scripts-configmap.yaml
│       │   ├── secret.yaml
│       │   ├── sentinel
│       │   │   ├── hpa.yaml
│       │   │   ├── node-services.yaml
│       │   │   ├── ports-configmap.yaml
│       │   │   ├── service.yaml
│       │   │   └── statefulset.yaml
│       │   ├── serviceaccount.yaml
│       │   ├── servicemonitor.yaml
│       │   └── tls-secret.yaml
│       ├── values.schema.json
│       └── values.yaml
├── Chart.yaml
├── images
│   ├── dashboard_export.png
│   ├── dashboard_import.png
│   ├── db_connect_error.png
│   ├── import_dashboard.png
│   ├── Readme.md
│   └── role_access.png
├── my-values.yaml
├── Readme.md
└── templates
    ├── deployment.yaml
    ├── _helpers.tpl
    ├── hpa.yaml
    ├── ingress.yaml
    ├── NOTES.txt
    ├── serviceaccount.yaml
    ├── service.yaml
    └── tests
        └── test-connection.yaml
"
This was obtained from https://superset.apache.org/docs/installation/running-on-kubernetes/. This repository adjusts the configurations for the ingress and OAUTH.

<!-- USAGE EXAMPLES -->
## Usage
These were the configurations made in order to run Superset on Kubernetes with Ingress and OAUTH.

### Dependencies
The additional dependencies of authlib,flask_oauthlib and pyhive were installed for the OAUTH and the usage of the Spark Thrift SQL server.

This is configured at line 38 of the bootstrapScript of the my-values.yaml. If you require additional dependencies, please input accordingly. A snippet of the values is as shown:
'''
bootstrapScript: |
  #!/bin/bash
  rm -rf /var/lib/apt/lists/* && \
  pip install \
    psycopg2-binary==2.9.1 \
    authlib \
    flask_oauthlib \
    pyhive \
    redis==3.5.3 && \
  if [ ! -f ~/bootstrap ]; then echo "Running Superset with uid {{ .Values.runAsUser }}" > ~/bootstrap; fi
'''
### Ingress
nginx was used to implement the ingress. Input the host name for the redirected url, an example could be organisation-superset.net.The following configurations can be seen in line 206 in my-value.yaml as shown:
'''
ingress:
  enabled: true
  # ingressClassName: nginx
  annotations:
    acme.cert-manager.io/http01-edit-in-place: "true"
    cert-manager.io/cluster-issuer: letsencrypt-prod
    cert-manager.io/issue-temporary-certificate: "true"
    kubernetes.io/ingress.class: nginx
    meta.helm.sh/release-name: superset
    # kubernetes.io/tls-acme: "true"
    ## Extend timeout to allow long running queries.
    # nginx.ingress.kubernetes.io/proxy-connect-timeout: "300"
    # nginx.ingress.kubernetes.io/proxy-read-timeout: "300"
    # nginx.ingress.kubernetes.io/proxy-send-timeout: "300"
  path: /
  pathType: Prefix
  hosts:
    - inputhostname
  tls:
  - hosts:
      - inputhostname
  # - secretName: chart-example-tls
  #    hosts:
  #      - chart-example.local
'''
### OAUTH
Obtain the required inputs for the OATUH from GCP. 

Insert the home domain for the users if its @gmail.com input gmail.com. This can be seen in line 78 from the my-values.yaml.
'''
OAUTH_HOME_DOMAIN: <insert OAUTH HOME DOMAIN>
'''
Input the google key & secret as well as the map box api token obtained in the prerequsites. This can be seen in line 94 from the my-values.yaml.
'''
extraSecretEnv:
  GOOGLE_KEY: ToBeUpdated
  GOOGLE_SECRET: ToBeUpdated
  MAPBOX_API_KEY: ToBeUpdated
'''

Input the variables for OAUTH providers as seen in line 141 from the my-values.yaml.
'''
configOverrides:
  enable_oauth: |
    # This will make sure the redirect_uri is properly computed, even with SSL offloading
    ENABLE_PROXY_FIX = True

    from flask_appbuilder.security.manager import AUTH_OAUTH
    AUTH_TYPE = AUTH_OAUTH
    OAUTH_PROVIDERS = [
        {
            "name": "google",
            "icon": "fa-google",
            "token_key": "access_token",
            "remote_app": {
                "client_id": os.getenv("GOOGLE_KEY"),
                "client_secret": os.getenv("GOOGLE_SECRET"),
                "api_base_url": "https://www.googleapis.com/oauth2/v2/",
                "client_kwargs": {"scope": "email profile"},
                "request_token_url": None,
                "access_token_url": "https://accounts.google.com/o/oauth2/token",
                "authorize_url": "https://accounts.google.com/o/oauth2/auth",
                "authorize_params": {"hd": os.getenv("AUTH_DOMAIN", "")},
            },
        }
    ]

    # Map Authlib roles to superset roles
    AUTH_ROLE_ADMIN = 'Admin'
    AUTH_ROLE_PUBLIC = 'Public'

    # Will allow user self registration, allowing to create Flask users from Authorized User
    AUTH_USER_REGISTRATION = True

    # The default user self registration role
    AUTH_USER_REGISTRATION_ROLE = "Admin"
'''

### Helm install
Assuming you already have Helm installed, execute the following command in your CLI.

'''
helm upgrade superset superset/superset --install --values my_values.yaml --namespace <insert namespace>
'''
Superset can now be used in the host name in the browser that was defined in the ingress.

### User 
For a user-friendly guide on how to use Superset, you can refer to this * [![post][post-url]] :)
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[post-url]: https://epoch.aisingapore.org/2023/01/apache-superset-an-open-source-visualization-tool/
[Helm-url]: https://helm.sh/
[Superset.js]: https://upload.wikimedia.org/wikipedia/commons/0/0e/Superset_logo.svg
[Superset-url]: https://superset.apache.org/
[GCP.js]: https://miro.medium.com/max/640/1*COzjCLTX2liPee-1JYsf_w.webp
[GoogleCloud-url]: https://cloud.google.com/free?utm_source=google&utm_medium=cpc&utm_campaign=japac-SG-all-en-dr-bkws-all-all-trial-e-dr-1009882&utm_content=text-ad-none-none-DEV_c-CRE_602258786551-ADGP_Hybrid%20%7C%20BKWS%20-%20EXA%20%7C%20Txt%20~%20GCP%20~%20General_%20Core%20Brand-KWID_43700071544383224-kwd-87853815-userloc_9062509&utm_term=KW_gcp-ST_gcp&gclid=Cj0KCQiAtvSdBhD0ARIsAPf8oNnkoVQxgOIh7OT44dUa-e5ffPvNLuuDMqcSIO87fvKGmBfgQHktTLkaAqLEEALw_wcB&gclsrc=aw.ds
[SparkThriftServer.js]: https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/Apache_Spark_logo.svg/250px-Apache_Spark_logo.svg.png
[Spark-url]: https://spark.apache.org/
