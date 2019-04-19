# Rick-SDC

app.get('/data/artist/:id', (req, res) => {
  const { id } = req.params;

  db.getArtist(id)
    .then(artist => res.json(artist))
    .catch(console.log);
});

  getArtistState(id) {
      fetch(`/data/artist/${id}`)
      .then(result => result.json())
      .then(data => {
        if (this._isMounted) {
          this.setState({ name: data.name, header_img: data.header_img})
        }
      })
  }