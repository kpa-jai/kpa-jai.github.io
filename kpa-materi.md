---
layout: page
title: Materi
permalink: /kpa/materi
---

### Jenis Materi

<table>
  <thead>
    <tr>
      <th>No.</th>
      <th>Kode</th>
      <th>Nama Pelajaran</th>
    </tr>
  </thead>
  <tbody>
  {% for db in site.data.db-materi %}
    <tr>
      <td>{{ db.no }}</td>
      <td>{{ db.kode }}</td>
      <td>{{ db.nama-pelajaran }}</td>
    </tr>
  {% endfor %}  
  </tbody>
</table>

### Daftar Materi

<!-- <ul>
  {% for category in site.categories %}
    <li>{{ category[0] }}</li>
    <ul>
      {% for post in category[1] %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
    </ul>
  {% endfor %}
</ul> -->

<!-- <table>
  <thead>
    <tr>
      <th>Category</th>
      <th>Posts</th>
    </tr>
  </thead>
  <tbody>
    {% for category in site.categories %}
      <tr>
        <td>{{ category[0] }}</td>
        <td>
          <ul>
            {% for post in category[1] %}
              <li><a href="{{ post.url }}">{{ post.title }}</a></li>
            {% endfor %}
          </ul>
        </td>
      </tr>
    {% endfor %}
  </tbody>
</table> -->

{% assign sorted_kurikulum = site.data.db-materi-kelas | sort: 'kelas' %}

<table>
  <thead>
    <tr>
      <!-- <th>No.</th> -->
      <th>Kelas</th>
      <th>Nama Pelajaran</th>
      <th>Link</th>
    </tr>
  </thead>
  <tbody>
  {% for db in sorted_kurikulum %}
    <tr>
      <!-- <td>{{ db.no }}</td> -->
      <td>{{ db.kelas }}</td>
      <td>{{ db.mata-pelajaran }}</td>
      <td><a href="{{ db.link-materi }}">{{ db.link-materi-web }}</a></td>
    </tr>
  {% endfor %}  
  </tbody>
</table>