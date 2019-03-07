# API Design

TOC:

- 1 Intro
- 2 RESTfull
- 3 URL Guidlines
- 3 API Methods
- 4 Error handling
- 4 Versioning
- 5 Caching

<img src="images/git_lifecycle.png" width="800px">

**References:** - Roy Fielding 'REST' publication in 2000.

## 0 History

    - RPC + xml
    - SOAP + xml

    Start of mobile devices:
        problem:
            - xml = heavy = CPU/Memrory intensive
            - xml = not human elegant-readable.

    Solution

    - REST = Represtational State Transfer
    - JSON = Javascript Simple Object Notation (2002 but popular starts 2006)

## 1 Intro

** API = Application Programm Interface **

What = - user interface to data and systems that is consumed by applications instead of humans. - strict **contract** between provider and consumer - contract: - url definition & versioning - definition of methods (POST,GET,...) + Headers + arguments / datatypes - structure of requests and responses

_Remark: Swagger is todays defacto standard to document this._

## 2 REST

- Communication protocol is defacto 'HTTP' but not mandatory

### 2.1 API types:

    - Public
    - Partner
    - Private

### 2.3 API management:

    - API-Security
    - Access Request
    - Documentation
    - SLA management

### 2.4 6 REST Architectoral Constraints.

Restfull ? = HTTP + JSON -> No = 'REST-like' or 'RESTisch'

RESTfull = 6 REST Architectoral Constraints:

    - Client-Server
    - Uniform Interface             = 'contract'
    - Statelessness                 = server does NOTmanage state of application
    - Caching                       = server controls caching of response via Headers
    - Layered system                = independly managed layers
    - Code On Demand (optional)     = server can send executable code via body in response

### 2.5 API value Chain:

    - API = a Product
    - API is made for the 'App developers':
        Advice:
            - Un-Ambiguous design
            - design for simplicity
            - be clear
            - Stay Consistent
            - ! Document

## API - Endpoint - Resources - Actions

    - API-Endpoint:
