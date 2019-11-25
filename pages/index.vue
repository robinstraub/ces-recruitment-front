<template>
  <b-container>
    {{/* player filters form */}}
    <form>
      <b-form-group label="ratio de winRate" label-for="winRate-range-input">
        <b-form-input id="winRate-range-input" type="range" min="0" max="100" />
      </b-form-group>
      <b-form-group label="ratio de winRate" label-for="winRate-range-input">
        <b-form-input id="winRate-range-input" type="range" min="0" max="100" />
      </b-form-group>
      <b-form-group label="ratio de winRate" label-for="winRate-range-input">
        <b-form-input id="winRate-range-input" type="range" min="0" max="100" />
      </b-form-group>
      <div class="text-center">
        <b-button variant="primary">Trouver mon athlète</b-button>
      </div>
    </form>
    {{/* matching players table */}}
    <b-table striped hover :items="players" :fields="fields" />
  </b-container>
</template>

<script>
export default {
    data() {
        return {
            fields: [
                { key: 'name', label: 'Name' },
                { key: 'winRate', label: 'Win Rate' },
                { key: 'championPool', label: 'Champion Pool' },
                { key: 'tiltedWinRate', label: 'Win Rate When Tilted' },
            ],
            players: [
                { id: 0, name: 'destrufion', winRate: '60%', championPool: '12', tiltedWinRate: '42%' },
                { id: 1, name: 'destrufion', winRate: '0.6', championPool: '12', tiltedWinRate: '42%' },
                { id: 2, name: 'destrufion', winRate: '60%', championPool: '12', tiltedWinRate: '42%' },
                { id: 3, name: 'destrufion', winRate: '60%', championPool: '12', tiltedWinRate: '42%' },
                { id: 4, name: 'destrufion', winRate: '60%', championPool: '12', tiltedWinRate: '42%' },
                { id: 5, name: 'destrufion', winRate: '60%', championPool: '12', tiltedWinRate: '42%' },
                { id: 6, name: 'destrufion', winRate: '60%', championPool: '12', tiltedWinRate: '42%' },
                { id: 7, name: 'destrufion', winRate: '60%', championPool: '12', tiltedWinRate: '42%' },
                { id: 8, name: 'destrufion', winRate: '60%', championPool: '12', tiltedWinRate: '42%' },
                { id: 9, name: 'destrufion', winRate: '60%', championPool: '12', tiltedWinRate: '42%' },
            ]
        }
    },
}
</script>
