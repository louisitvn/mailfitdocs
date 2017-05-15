## 1. Introduction

MailFit provides RESTful API which is based on simple `HTTP POST/GET` requests. We make it easy and quick to integrate MailFit sending capability with your website or application. Our API lets you create, manage, send, schedule campaigns as well as track your delivery statistics.

## 2. API Reference

### LIST

#### GET /api/v1/lists

Get all mail lists' information

```sh
curl -X GET -H "accept:application/json" -G \
http://test.mailfit.com:8888/api/v1/lists? \
-d api_token=ME45Scg0tKaDplHgvR7Pcv20o9RsNna9dxx39lsayRpKkCZkP9QAgqT10yL7
```

#### GET /api/v1/lists/{uid}

Retrieve a particular list's information

```sh
curl -X GET -H "accept:application/json" -G \
http://test.mailfit.com:8888/api/v1/lists/{uid}? \
-d api_token=ME45Scg0tKaDplHgvR7Pcv20o9RsNna9dxx39lsayRpKkCZkP9QAgqT10yL7
```

### CAMPAIGN

#### GET /api/v1/campaigns

Get all campaigns' information

```sh
curl -X GET -H "accept:application/json" -G \
http://test.mailfit.com:8888/api/v1/campaigns? \
-d api_token=ME45Scg0tKaDplHgvR7Pcv20o9RsNna9dxx39lsayRpKkCZkP9QAgqT10yL7
```

#### GET /api/v1/campaigns/{uid}

Retrieve a particular campaign's information

```sh
curl -X GET -H "accept:application/json" -G \
http://test.mailfit.com:8888/api/v1/campaigns/{uid}? \
-d api_token=ME45Scg0tKaDplHgvR7Pcv20o9RsNna9dxx39lsayRpKkCZkP9QAgqT10yL7
```

### SUBSCRIBER

#### GET /api/v1/lists/{list_uid}/subscribers

Get all subscribers of a mail list

Parameters:

* `list_uid` Mail list's UID

```sh
curl -X GET -H "accept:application/json" -G \
http://test.mailfit.com:8888/api/v1/lists/{list_uid}/subscribers? \
-d api_token=ME45Scg0tKaDplHgvR7Pcv20o9RsNna9dxx39lsayRpKkCZkP9QAgqT10yL7
```

#### GET /api/v1/lists/{list_uid}/subscribers/{uid}

Retrive a particulr subscriber of a mail list

Parameters:

* `list_uid` Mail list's UID
* `uid` Subscriber's UID

```sh
curl -X GET -H "accept:application/json" -G \
http://test.mailfit.com:8888/api/v1/lists/{list_uid}/subscribers/{uid}? \
-d api_token=ME45Scg0tKaDplHgvR7Pcv20o9RsNna9dxx39lsayRpKkCZkP9QAgqT10yL7
```


#### PATCH /api/v1/lists/{list_uid}/subscribers/{uid}/subscribe

Subscribe a subscriber

Parameters:

* `list_uid` Mail list's UID
* `uid` Subscriber's UID

```sh
curl -X PATCH -H "accept:application/json" -G \
http://test.mailfit.com:8888/api/v1/lists/{list_uid}/subscribers/{uid}/subscribe? \
-d api_token=ME45Scg0tKaDplHgvR7Pcv20o9RsNna9dxx39lsayRpKkCZkP9QAgqT10yL7
```

#### PATCH /api/v1/lists/{list_uid}/subscribers/{uid}/unsubscribe

Unsubscribe a subscriber

Parameters:

* `list_uid` Mail list's UID
* `uid` Subscriber's UID

```sh
curl -X PATCH -H "accept:application/json" -G \
http://test.mailfit.com:8888/api/v1/lists/{list_id}/subscribers/{uid}/unsubscribe? \
-d api_token=ME45Scg0tKaDplHgvR7Pcv20o9RsNna9dxx39lsayRpKkCZkP9QAgqT10yL7
```
