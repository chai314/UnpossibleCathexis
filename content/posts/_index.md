<script src="https://cdn.jsdelivr.net/npm/typeit@7.0.4/dist/typeit.min.js"></script>

<h1>
<p id="Sos"></p>
<script>
new TypeIt("#Sos", { 
    lifeLike: false, 
    speed: 0 
})
	.type("Style over substance", {speed:50})
    .pause(1000)
	.move(-10, {speed: 100})
	.pause(450)
	.delete(4, {speed: 50})
	.type("is", {speed:50})
	.pause(450)
	.move(10, {speed: 100})
	.pause(450)
	.type(".")
	.go();
</script>
</h1>