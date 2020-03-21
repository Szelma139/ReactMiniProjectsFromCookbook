import React, {Component} from 'react';
import { StyleSheet, Text, View, TouchableHighlight, ImageBackground, Image } from 'react-native';

const playIcon = require('./images/play.png');
const volumeIcon = require('./images/sound.png');
const hdIcon = require('./images/hd-sign.png');
const fullScreenIcon = require('./images/full-screen.png');
const flower = require('./images/flower.jpg');
const remoteImage = { uri:
`https://farm5.staticflickr.com/4702/24825836327_bb2e0fc39b_b.jpg`
};
const heartIcon = require('./images/heart.png');


export default class App extends React.Component {
  state = {
    liked: false, //stan czy polubiony
  };
  handleButtonPress = () => {
    this.setState({
      liked: !this.state.liked,
    });
  }
  render() {
    const likedStyles = this.state.liked ? styles.liked :   //jesli true to polubiony i ustaw tablice na styl z const styles, kolor na czerwony
undefined;
    return (
      <View style={styles.container}>
        <TouchableHighlight
          onPress={this.handleButtonPress}
          style={styles.button}
          underlayColor="#fefefe"
        >
          <Image
            source={heartIcon}
            style={[styles.icon, likedStyles]}
          />
        </TouchableHighlight>
        <Text style={styles.text}>Do you like this app?</Text>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    marginTop: 50,
    alignItems: 'center',
  },
  button: {
    borderRadius: 5,
    padding: 10,
  },
  icon: {
    width: 180,
    height: 180,
    tintColor: '#f1f1f1',
  },
  liked: {
    tintColor: '#e74c3c',
  },
  text: {
    marginTop: 20,
  },
});
