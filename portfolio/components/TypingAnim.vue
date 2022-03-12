<template>
  <div ref="typing" class="typing-anim" />
</template>

<script>
export default {
  name: 'TypingAnim',
  props: {
    text: {
      type: String,
      required: true
    },
    speed: {
      type: Number,
      default: 100
    },
    delay: {
      type: Number,
      default: 0
    }
  },
  data () {
    return {
      lines: [],
      currentLine: 0,
      cursor: 0,
      timestamp: 0,
      element: undefined
    }
  },
  mounted () {
    this.$refs.typing.innerHTML = ''

    this.lines = this.text.split('\\n')
    this.createNewLine()

    setTimeout(() => {
      requestAnimationFrame(timestamp => this.typing(timestamp))
    }, this.delay)
  },
  methods: {
    createNewLine () {
      if (this.element) {
        this.element.classList.remove('active')
      }

      this.element = document.createElement('p')
      this.element.classList.add('active')

      this.$refs.typing.appendChild(this.element)
    },
    typing (timestamp) {
      const diffTime = timestamp - this.timestamp

      if (diffTime < this.speed) {
        requestAnimationFrame(timestamp => this.typing(timestamp))
        return
      } else if (this.currentLine >= this.lines.length) {
        this.element.classList.remove('active')
        return
      } else if (this.cursor === 0 && this.currentLine > 0) {
        this.createNewLine()
      }

      this.element.innerHTML += this.lines[this.currentLine][this.cursor]
      this.cursor++

      if (this.cursor >= this.lines[this.currentLine].length) {
        this.cursor = 0
        this.currentLine++
      }

      // Update Timestamp
      this.timestamp = timestamp

      // Next Frame
      requestAnimationFrame(timestamp => this.typing(timestamp))
    }
  }
}
</script>

<style>
  @keyframes typing-cursor-blink {
    from { color: white; }
    50% { color: coral; }
    to { color: white; }
  }

  .typing-anim p {
    margin: 0;
  }

  .typing-anim p.active::after {
    content: '|';
    font-weight: bold;
    margin: 0 3px;
    color: coral;
    animation: typing-cursor-blink 1s infinite;
  }
</style>
