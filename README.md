# Rare iOS URL Schemes

Every scheme added to this list is, at time of writing, either:

- _Found by me:_ No prior search results

- _Found by [someone else](#anchor-credit):_ At __most__ one prior search result

## Settings

### Apple Account

#### Open Settings → Apple Account → iCloud → Photos

```bash
prefs:root=APPLE_ACCOUNT&path=ICLOUD_SERVICE/com.apple.Dataclass.Photos
```

### Apps

#### Open Settings → Apps

> [!IMPORTANT]
> _Prerequisite:_ Uninstall `Apple Books` app.

```bash
prefs:root=IBOOKS
```

## First-Party Apps

### App Store

#### App Updates

```bash
itms-apps://itunes.apple.com/updates
```

### Photos

#### Albums (All)

```bash
photos-navigation://album
```

#### Bursts

```bash
photos://album?name=bursts
```

#### Favorites

```bash
photos://album?name=favorites
```

[^1]

#### Hidden

```bash
photos://album?name=hidden
```

#### Imported

> [!WARNING]
> iOS 18.0.1: `all-imported` and `last-imported` fail

- All [^1]

  ```bash
  photos-navigation://all-imported
  ``` 

- Last (Most Recent) [^1]
  
  ```bash
  photos-navigation://last-imported
  ```

#### Memories

```bash
photos-navigation://memories
```

[^1]

#### One Year Ago

```bash
photos://oneyearago
```

[^1]

#### People and Pets

```bash
photos://people
```

[^1]

#### Recently Deleted

```bash
photos://album?name=recently-deleted
```

[^1]

#### Screenshots

```bash
photos://album?name=screenshots
```

#### Trips

```bash
photos://trips
```

#### Videos

```bash
photos://album?name=videos
```

## Third-Party Apps

### Amazon

#### Subscribe & Save

- Upcoming Deliveries

  - Coming soon

- Subscriptions (Active)

  - Coming soon

- Subscriptions (Canceled)

  - Coming soon
  
### Google Calendar

#### Views

##### Day (Today or Date)

- Today

  ```bash
  https://calendar.google.com/calendar/u/0/r/day
  ```

- Date (yyyy/MM/dd)

  ```bash
  https://calendar.google.com/calendar/u/0/r/day/2024/10/21
  ```

##### 3 Day (Today or Date)

- Today

  ```bash
  https://calendar.google.com/calendar/u/0/r/3day
  ```

- Date (yyyy/MM/dd, e.g. 2024/10/21)

  ```bash
  https://calendar.google.com/calendar/u/0/r/3day/2024/10/21
  ```

##### Week (Today or Date)

- Today

  ```bash
  https://calendar.google.com/calendar/u/0/r/week
  ```

- Date (yyyy/MM/dd, e.g. 2024/10/21)

  ```bash
  https://calendar.google.com/calendar/u/0/r/week/2024/10/21
  ```

##### Month (Today or Date)

- Today

  ```bash
  https://calendar.google.com/calendar/u/0/r/month
  ```

- Date (yyyy/MM/dd, e.g. 2024/10/21)

  ```bash
  https://calendar.google.com/calendar/u/0/r/month/2024/10/21
  ```

##### Agenda (Today or Date)

- Today

  ```bash
  https://calendar.google.com/calendar/u/0/r/agenda
  ```

- Date (yyyy/MM/dd, e.g. 2024/10/21)

  ```bash
  https://calendar.google.com/calendar/u/0/r/agenda/2024/10/21
  ```

#### Events

##### Create Event with Title, Description, Location, Attendees, Is All-Day, Start Date, End Date

```bash
googlecalendar://?action=&title=&description=&location=&add=&isallday=&dates=
```

- Explanation

  ```bash
  googlecalendar://?
    action=create
    &title=TITLE
    &description=DESCRIPTION
    &location=LOCATION
    &add=EMAIL1,EMAIL2,EMAIL_N
    &isallday=ZERO_OR_ONE
    &dates=START_UTC_yyyyMMddThhmmssZ/END_UTC_yyyyMMddThhmmssZ
  ```

- Example: `Cool Event` in `Seattle, WA` on October 21, 2024 from 7:30 AM – 9:30 AM Seattle local time

  ```bash
  googlecalendar://?action=create&title=Cool%20Event&description=Come%20through!&location=Seattle,%20WA&add=foo@example.com,bar@example.com&isallday=0&dates=20241021T143000Z/20241021T163000Z
  ```

##### Edit Existing Event

Coming soon

##### Open Calendar to View Existing Event

Coming soon

### LG

```bash
com.lgeha.nuts://
```

<a name="anchor-credit"></a>

[^1]: [Sami Samhuri](https://samhuri.net/posts/2024/04/photos-navigation-url-scheme)