# chickenstats-api

API for downloading NHL data

- API version: 0.1.4
- Package version: 0.1.4

## Requirements

Python 3.9+

## Installation

```sh
pip install chickenstats-api
```

```python
import chickenstats_api
```

## Getting Started

```python

import chickenstats_api
from chickenstats_api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.chickenstats.com
# See configuration.py for a list of all supported configuration parameters.
configuration = chickenstats_api.Configuration(
    host = "https://api.chickenstats.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]


# Enter a context with an instance of the API client
with chickenstats_api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = chickenstats_api.LinesApi(api_client)
    season = [56] # List[int] |  (optional)
    sessions = ['sessions_example'] # List[str] |  (optional)
    game_id = [56] # List[int] |  (optional)
    team = ['team_example'] # List[str] |  (optional)
    opp_team = ['opp_team_example'] # List[str] |  (optional)
    strength_state = ['strength_state_example'] # List[str] |  (optional)
    score_state = True # bool |  (optional)
    level = 'level_example' # str |  (optional)
    linemates = True # bool |  (optional)
    opposition = True # bool |  (optional)
    limit = 10000 # int |  (optional) (default to 10000)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # Read Game Lines
        api_response = api_instance.read_game_lines(season=season, sessions=sessions, game_id=game_id, team=team, opp_team=opp_team, strength_state=strength_state, score_state=score_state, level=level, linemates=linemates, opposition=opposition, limit=limit, offset=offset)
        print("The response of LinesApi->read_game_lines:\n")
        pprint(api_response)
    except ApiException as e:
        print("Exception when calling LinesApi->read_game_lines: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *https://api.chickenstats.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*LinesApi* | [**read_game_lines**](docs/LinesApi.md#read_game_lines) | **GET** /api/v1/chicken_nhl/lines/game | Read Game Lines
*LinesApi* | [**read_line_ids**](docs/LinesApi.md#read_line_ids) | **GET** /api/v1/chicken_nhl/lines/line_ids | Read Line Ids
*LinesApi* | [**read_lines_game_ids**](docs/LinesApi.md#read_lines_game_ids) | **GET** /api/v1/chicken_nhl/lines/game_ids | Read Lines Game Ids
*LinesApi* | [**read_season_lines**](docs/LinesApi.md#read_season_lines) | **GET** /api/v1/chicken_nhl/lines/season | Read Season Lines
*LoginApi* | [**login_auth0_token**](docs/LoginApi.md#login_auth0_token) | **POST** /api/v1/login/auth0-token | Login Auth0 Token
*LoginApi* | [**login_callback**](docs/LoginApi.md#login_callback) | **POST** /api/v1/login/callback | Login Callback
*LoginApi* | [**recover_password**](docs/LoginApi.md#recover_password) | **POST** /api/v1/password-recovery/{email} | Recover Password
*LoginApi* | [**recover_password_html_content**](docs/LoginApi.md#recover_password_html_content) | **POST** /api/v1/password-recovery-html-content/{email} | Recover Password Html Content
*LoginApi* | [**reset_password**](docs/LoginApi.md#reset_password) | **POST** /api/v1/reset-password/ | Reset Password
*LoginApi* | [**test_token**](docs/LoginApi.md#test_token) | **POST** /api/v1/login/test-token | Test Token
*PlayByPlayApi* | [**read_pbp**](docs/PlayByPlayApi.md#read_pbp) | **GET** /api/v1/chicken_nhl/play_by_play | Read Pbp
*PlayByPlayApi* | [**read_pbp_game_ids**](docs/PlayByPlayApi.md#read_pbp_game_ids) | **GET** /api/v1/chicken_nhl/play_by_play/game_ids | Read Pbp Game Ids
*PlayByPlayApi* | [**read_pbp_play_ids**](docs/PlayByPlayApi.md#read_pbp_play_ids) | **GET** /api/v1/chicken_nhl/play_by_play/play_ids | Read Pbp Play Ids
*StatsApi* | [**read_game_stats**](docs/StatsApi.md#read_game_stats) | **GET** /api/v1/chicken_nhl/stats/game | Read Game Stats
*StatsApi* | [**read_season_stats**](docs/StatsApi.md#read_season_stats) | **GET** /api/v1/chicken_nhl/stats/season | Read Season Stats
*StatsApi* | [**read_stats_game_ids**](docs/StatsApi.md#read_stats_game_ids) | **GET** /api/v1/chicken_nhl/stats/game_ids | Read Stats Game Ids
*TeamStatsApi* | [**read_game_team_stats**](docs/TeamStatsApi.md#read_game_team_stats) | **GET** /api/v1/chicken_nhl/team_stats/game | Read Game Team Stats
*TeamStatsApi* | [**read_season_team_stats**](docs/TeamStatsApi.md#read_season_team_stats) | **GET** /api/v1/chicken_nhl/team_stats/season | Read Season Team Stats
*TeamStatsApi* | [**read_team_stats_game_ids**](docs/TeamStatsApi.md#read_team_stats_game_ids) | **GET** /api/v1/chicken_nhl/team_stats/game_ids | Read Team Stats Game Ids
*TeamStatsApi* | [**read_team_stats_ids**](docs/TeamStatsApi.md#read_team_stats_ids) | **GET** /api/v1/chicken_nhl/team_stats/team_stats_ids | Read Team Stats Ids
*UsersApi* | [**delete_user_me**](docs/UsersApi.md#delete_user_me) | **DELETE** /api/v1/users/me | Delete User Me
*UsersApi* | [**get_programmatic_credentials**](docs/UsersApi.md#get_programmatic_credentials) | **GET** /api/v1/users/me/programmatic-credentials | Get Programmatic Credentials
*UsersApi* | [**read_user_me**](docs/UsersApi.md#read_user_me) | **GET** /api/v1/users/me | Read User Me
*UsersApi* | [**resend_verification**](docs/UsersApi.md#resend_verification) | **POST** /api/v1/users/me/resend-verification | Resend Verification
*UsersApi* | [**rotate_programmatic_credentials**](docs/UsersApi.md#rotate_programmatic_credentials) | **POST** /api/v1/users/me/programmatic-credentials/rotate | Rotate Programmatic Credentials
*UsersApi* | [**signup**](docs/UsersApi.md#signup) | **POST** /api/v1/users/signup | Signup
*UsersApi* | [**sync_ghost_tier**](docs/UsersApi.md#sync_ghost_tier) | **POST** /api/v1/users/me/sync-ghost | Sync Ghost Tier
*UsersApi* | [**update_password_me**](docs/UsersApi.md#update_password_me) | **PATCH** /api/v1/users/me/password | Update Password Me
*UsersApi* | [**update_user_me**](docs/UsersApi.md#update_user_me) | **PATCH** /api/v1/users/me | Update User Me


## Documentation For Models

 - [HTTPValidationError](docs/HTTPValidationError.md)
 - [LinesCreate](docs/LinesCreate.md)
 - [LinesGame](docs/LinesGame.md)
 - [LinesGameResponse](docs/LinesGameResponse.md)
 - [LinesPublic](docs/LinesPublic.md)
 - [LinesSeason](docs/LinesSeason.md)
 - [LinesSeasonResponse](docs/LinesSeasonResponse.md)
 - [Message](docs/Message.md)
 - [NewPassword](docs/NewPassword.md)
 - [PbpPublic](docs/PbpPublic.md)
 - [PbpResponse](docs/PbpResponse.md)
 - [ProgrammaticCredentials](docs/ProgrammaticCredentials.md)
 - [StatsCreate](docs/StatsCreate.md)
 - [StatsGame](docs/StatsGame.md)
 - [StatsGameResponse](docs/StatsGameResponse.md)
 - [StatsSeason](docs/StatsSeason.md)
 - [StatsSeasonResponse](docs/StatsSeasonResponse.md)
 - [TeamStatsCreate](docs/TeamStatsCreate.md)
 - [TeamStatsGame](docs/TeamStatsGame.md)
 - [TeamStatsGameResponse](docs/TeamStatsGameResponse.md)
 - [TeamStatsPublic](docs/TeamStatsPublic.md)
 - [TeamStatsSeason](docs/TeamStatsSeason.md)
 - [TeamStatsSeasonResponse](docs/TeamStatsSeasonResponse.md)
 - [Token](docs/Token.md)
 - [UpdatePassword](docs/UpdatePassword.md)
 - [UserCreate](docs/UserCreate.md)
 - [UserPublic](docs/UserPublic.md)
 - [UserRegister](docs/UserRegister.md)
 - [UserUpdate](docs/UserUpdate.md)
 - [UserUpdateMe](docs/UserUpdateMe.md)
 - [UsersPublic](docs/UsersPublic.md)
 - [ValidationError](docs/ValidationError.md)
 - [ValidationErrorLocInner](docs/ValidationErrorLocInner.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization


Authentication schemes defined for the API:
<a id="OAuth2PasswordBearer"></a>
### OAuth2PasswordBearer

- **Type**: OAuth
- **Flow**: password
- **Authorization URL**: 
- **Scopes**: N/A


## Author

chicken@chickenandstats.com


