<script>
	const { data } = $props()
</script>

<Wrapper>
	<h1>Events</h1>
	<Client browser>
		{#if data.events.length}
			<ol class="$flex $flex-column $gap">
				{#each data.events as event (event.id)}
					<XioniEventTile tag="li" {event} />
				{/each}
			</ol>
		{:else}
			<p>
				<Fontello name="attention" />
				Zur Zeit sind keine Veranstaltungen geplant.
			</p>
		{/if}
	</Client>
</Wrapper>
