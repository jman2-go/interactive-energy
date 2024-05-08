<script>
	import * as d3 from 'd3';

    var lineGenerator = d3.line();

    var points = [];
    for(let i = 0; i < 200; i++)
        points.push([ i * 3, Math.random() * 100 ]);

    var pathData = lineGenerator(points);

</script>

<div class="visualization">
	<svg width="500" height="500">
		<g transform="translate(250, 120)">
			<path 
				d={pathData}
			/>
		</g>
	</svg>
</div>

<style>
    path {
	fill: none;
	stroke: #999;
}
</style>
