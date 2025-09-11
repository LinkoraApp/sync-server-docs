# Database Setup

## Database URL Formats

<table style="width:100%; border-collapse: collapse; margin-top: 1.5em; margin-bottom: 1.5em; border: 1px solid #444;">
  <thead>
    <tr style="background-color: #363953; color: #E8EBFD; text-align: left;">
      <th style="padding: 10px; border: 1px solid #444; font-family: Inter, sans-serif;">Database</th>
      <th style="padding: 10px; border: 1px solid #444; font-family: Inter, sans-serif;">URL Format</th>
    </tr>
  </thead>
  <tbody>
    <tr style="background-color: #2F3146; color: #C2C7E4;">
      <td style="padding: 10px; border: 1px solid #444; font-family: Inter, sans-serif;">MySQL</td>
      <td style="padding: 10px; border: 1px solid #444; font-family: Inter, sans-serif;"><code>mysql://hostname:port/database_name</code></td>
    </tr>
    <tr style="background-color: #2F3146; color: #C2C7E4;">
      <td style="padding: 10px; border: 1px solid #444; font-family: Inter, sans-serif;">PostgreSQL</td>
      <td style="padding: 10px; border: 1px solid #444; font-family: Inter, sans-serif;"><code>postgresql://hostname:port/database_name</code></td>
    </tr>
    <tr style="background-color: #2F3146; color: #C2C7E4;">
      <td style="padding: 10px; border: 1px solid #444; font-family: Inter, sans-serif;">SQLite</td>
      <td style="padding: 10px; border: 1px solid #444; font-family: Inter, sans-serif;"><code>sqlite:/path/to/database/file.db</code></td>
    </tr>
  </tbody>
</table>


## Important Notes
- For SQLite, leave `databaseUser` and `databasePassword` empty
- The server has been tested with MySQL, SQLite, and PostgreSQL
- Other databases supported by [JetBrains Exposed](https://github.com/JetBrains/Exposed) may work but are untested
