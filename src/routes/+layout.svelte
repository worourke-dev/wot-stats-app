<TopAppBar bind:this={topAppBar} variant="standard">
    <Row>
        <Section>
        <IconButton class="material-icons">menu</IconButton>
        <Title>Squilliam's WoT Stats</Title>
        </Section>
        <Section align="end" toolbar>
        <IconButton class="material-icons" aria-label="Download"
            >file_download</IconButton
        >
        <IconButton class="material-icons" aria-label="Print this page"
            >print</IconButton
        >
        <IconButton class="material-icons" aria-label="Bookmark this page"
            >bookmark</IconButton
        >
        </Section>
    </Row>
</TopAppBar>
<AutoAdjust {topAppBar}>
    <slot />
</AutoAdjust>

<script lang="ts">
    import TopAppBar, {
        Row,
        Section,
        Title,
        AutoAdjust,
    } from '@smui/top-app-bar';
    import IconButton from '@smui/icon-button';

    let topAppBar: TopAppBar;
</script>